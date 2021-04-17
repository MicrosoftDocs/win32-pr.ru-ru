---
description: Класс устройств связи/Dataport состоит из модемных устройств.
ms.assetid: 6bc314c6-30ec-4318-856a-3ab2fa6aadfb
title: канал связи/Dataport
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89210bcf14931e3905f71cdbb8678f5519cc4c3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682928"
---
# <a name="commdatamodem"></a>канал связи/Dataport

Класс устройств связи/Dataport состоит из модемных устройств. Доступ к этим устройствам осуществляется с помощью функций [File](/windows/desktop/FileIO/file-management-functions) и [Communications](/windows/desktop/DevIO/communications-functions). Устройства в этом классе связаны с линейными устройствами, поддерживающими \_ тип мультимедиа линемедиамоде данных, который указан в элементе **Двмедиамодес** структуры [**линедевкапс**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) для линейного устройства.

Функция [**линежетид**](/windows/desktop/api/Tapi/nf-tapi-linegetid) заполняет структуру [**варстринг**](/windows/desktop/api/Tapi/ns-tapi-varstring) , настроив **ДВСТРИНГФОРМАТ** на \_ двоичное значение STRINGFORMAT и добавляя следующие дополнительные члены:

``` syntax
HANDLE hComm;            // file handle to data modem
CHAR   szDeviceName[1];  // name of data modem
```

Элемент **хкомм** — это маркер открытого порта связи. Этот элемент имеет **значение NULL** , если порт еще не открыт, или если параметр *двселект* параметра [**ЛИНЕЖЕТИД**](/windows/desktop/api/Tapi/nf-tapi-linegetid) не является \_ значением вызова линекаллселект. Если вызов активен, поставщик услуг обычно открывает сам порт, чтобы получить прямое управление коммуникационной аппаратурой, но требуется только возвратить допустимый маркер, если линия подключена. Поставщик услуг открывает порт с использованием \_ \_ перекрывающегося значения флага файла, а затем настраивает порт с помощью параметров, заданных функцией [**линесетдевконфиг**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) . Можно задать дополнительные параметры конфигурации для устройства с помощью функций связи с возвращенным маркером.

Элемент **сздевиценаме** является строкой, завершающейся **нулем**, которая указывает имя порта связи, связанного со строкой, адресом или вызовом.

Если **хкомм** является допустимым маркером, его можно использовать при последующих вызовах файловых функций, таких как [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) и [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), для отправки и получения данных в вызове. Когда вы завершите использование порта связи и, прежде чем использовать функцию [**линедеаллокатекалл**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) для освобождения вызова, необходимо закрыть порт с помощью функции [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) .

При использовании функций [**линежетдевконфиг**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) и [**линесетдевконфиг**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) некоторым поставщикам служб требуется, чтобы данные конфигурации для этого класса устройств имели следующий формат:

``` syntax
typedef struct  tagDEVCFG  {
  DEVCFGHDR   dfgHdr;
  COMMCONFIG  commconfig;
} DEVCFG, *PDEVCFG, FAR* LPDEVCFG;

// Device setting information
typedef struct  tagDEVCFGDR  {
  DWORD       dwSize;
  DWORD       dwVersion;
  WORD        fwOptions;
  WORD        wWaitBong;
} DEVCFGHDR;
```

Ниже приведены сведения о конфигурации устройства для использования с функциями [**линежетдевконфиг**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) и [**линесетдевконфиг**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) .

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**двсизе**
</dt> <dd>

Сумма размера структуры **девкфгхдр** и фактического размера структуры [**коммконфиг**](/windows/desktop/api/winbase/ns-winbase-commconfig) .

</dd> <dt>

<span id="dwVersion"></span><span id="dwversion"></span><span id="DWVERSION"></span>**двверсион**
</dt> <dd>

Номер версии структуры **Девконфиг** Unimodem. Этот член может иметь \_ версию мдмкфг (0x00010003).

</dd> <dt>

<span id="fwOptions"></span><span id="fwoptions"></span><span id="FWOPTIONS"></span>**фвоптионс**
</dt> <dd>

Флаги параметров, которые отображаются на странице параметров Unimodem. Этот элемент может быть сочетанием следующих значений:

<dl> <dt>

<span id="TERMINAL_PRE__1_"></span><span id="terminal_pre__1_"></span>ТЕРМИНАЛ \_ до (1)
</dt> <dd>

Отображает экран предварительного терминала.

</dd> <dt>

<span id="TERMINAL_POST__2_"></span><span id="terminal_post__2_"></span>\_Запись терминала (2)
</dt> <dd>

Отображает экран после терминала.

</dd> <dt>

<span id="MANUAL_DIAL__4_"></span><span id="manual_dial__4_"></span>РУЧНОЙ \_ набор номера (4)
</dt> <dd>

Набирает телефон вручную, если это возможно.

</dd> <dt>

<span id="LAUNCH_LIGHTS__8_"></span><span id="launch_lights__8_"></span>\_Индикаторы запуска (8)
</dt> <dd>

Отображает значок модема в области состояние панели задач.

\_По умолчанию устанавливается только значение индикатора запуска

</dd> </dl> </dd> <dt>

<span id="wWaitBong"></span><span id="wwaitbong"></span><span id="WWAITBONG"></span>**вваитбонг**
</dt> <dd>

Число секунд (с детализацией в две секунды) для замены ожидания гудка ($).

</dd> <dt>

<span id="Commconfig"></span><span id="commconfig"></span><span id="COMMCONFIG"></span>**коммконфиг**
</dt> <dd>

Структура [**коммконфиг**](/windows/desktop/api/winbase/ns-winbase-commconfig) , которую можно использовать с функциями настройки связи и модема.

</dd> </dl>

 

 
