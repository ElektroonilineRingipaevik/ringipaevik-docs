# ✅🧑 Nõusolek Isikuandmete Töötlemiseks  {#nõusolek-isikuandmed}

## 📌 Назначение листа

В данном листе фиксируются разрешения от родителя (опекуна) на публикацию и обработку личных данных ребёнка, а также на их использование в определённых каналах распространения.

---

## 🔧 Реализованный функционал

### 📋 Глобальное и индивидуальное управление флажками {#checkbox-synchronization}

- Установка флажка (галочки) в ячейке **столбца G** активирует **все 11 чекбоксов** в диапазоне **H:R** соответствующей строки.
- Пользователь может вручную ставить или снимать флажки в отдельных ячейках диапазона H:R.
- Если **хотя бы один чекбокс** в диапазоне H:R **не установлен**:
  - ячейка G:
    - **окрашивается в жёлтый цвет**;
    - получает **примечание**;
    - **флажок снимается**.
- Если пользователь вручную установит флажки во **всех 11 ячейках H:R**, то:
  - глобальный флажок в G **установится автоматически**;
  - **заливка и примечание исчезнут**.
- Если установлен флажок в G и пользователь **снимает его вручную**, то:
  - **все флажки в H:R автоматически снимаются**;
  - ячейка G получает **жёлтую заливку** и **примечание**.

### 🔄 Синхронизация с другим листом {#checkbox-sync-with-oppijate}

- Чекбокс **столбца G** на этом листе синхронизирован с чекбоксом **столбца R** на листе [`🧑 Õppijate Nimekiri`](#oppijate-nimekiri).
- Изменения в одном листе автоматически отображаются в другом.

### 🛑 Блокировка флажков при отсутствии имени или фамилии {#disable-checkboxes}

- Все чекбоксы в диапазоне **G5:R** становятся **неактивными**, если:
  - в строке **не указаны имя или фамилия** (ячейки в столбцах **C или D** пусты).
- При попытке взаимодействия с такими чекбоксами появляется **всплывающее предупреждение**.

---

## 🧠 Реализация

- Функциональность реализована с помощью **Google Apps Script**.
- Используются:
  - **обработка события `onEdit(e)`**;
  - **логика синхронизации флажков**;
  - **управление примечаниями и заливкой**;
  - **условное форматирование** для деактивации ячеек.
