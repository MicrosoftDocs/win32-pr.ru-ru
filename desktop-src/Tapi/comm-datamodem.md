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
# <a name="commdatamodem"></a><span data-ttu-id="bfa9c-103">канал связи/Dataport</span><span class="sxs-lookup"><span data-stu-id="bfa9c-103">comm/datamodem</span></span>

<span data-ttu-id="bfa9c-104">Класс устройств связи/Dataport состоит из модемных устройств.</span><span class="sxs-lookup"><span data-stu-id="bfa9c-104">The comm/datamodem device class consists of datamodem devices.</span></span> <span data-ttu-id="bfa9c-105">Доступ к этим устройствам осуществляется с помощью функций [File](/windows/desktop/FileIO/file-management-functions) и [Communications](/windows/desktop/DevIO/communications-functions).</span><span class="sxs-lookup"><span data-stu-id="bfa9c-105">You access these devices by using the [file](/windows/desktop/FileIO/file-management-functions) and [communications functions](/windows/desktop/DevIO/communications-functions).</span></span> <span data-ttu-id="bfa9c-106">Устройства в этом классе связаны с линейными устройствами, поддерживающими \_ тип мультимедиа линемедиамоде данных, который указан в элементе **Двмедиамодес** структуры [**линедевкапс**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) для линейного устройства.</span><span class="sxs-lookup"><span data-stu-id="bfa9c-106">Devices in this class are associated with line devices that support the LINEMEDIAMODE\_DATAMODEM media type, which is specified in the **dwMediaModes** member of the [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) structure for the line device.</span></span>

<span data-ttu-id="bfa9c-107">Функция [**линежетид**](/windows/desktop/api/Tapi/nf-tapi-linegetid) заполняет структуру [**варстринг**](/windows/desktop/api/Tapi/ns-tapi-varstring) , настроив **ДВСТРИНГФОРМАТ** на \_ двоичное значение STRINGFORMAT и добавляя следующие дополнительные члены:</span><span class="sxs-lookup"><span data-stu-id="bfa9c-107">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) function fills a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting **dwStringFormat** to the STRINGFORMAT\_BINARY value and appending these additional members:</span></span>

``` syntax
HANDLE hComm;            // file handle to data modem
CHAR   szDeviceName[1];  // name of data modem
```

<span data-ttu-id="bfa9c-108">Элемент **хкомм** — это маркер открытого порта связи.</span><span class="sxs-lookup"><span data-stu-id="bfa9c-108">The **hComm** member is the handle of the open communications port.</span></span> <span data-ttu-id="bfa9c-109">Этот элемент имеет **значение NULL** , если порт еще не открыт, или если параметр *двселект* параметра [**ЛИНЕЖЕТИД**](/windows/desktop/api/Tapi/nf-tapi-linegetid) не является \_ значением вызова линекаллселект.</span><span class="sxs-lookup"><span data-stu-id="bfa9c-109">This member is **NULL** if the port is not yet open or if the *dwSelect* parameter of [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) is not the LINECALLSELECT\_CALL value.</span></span> <span data-ttu-id="bfa9c-110">Если вызов активен, поставщик услуг обычно открывает сам порт, чтобы получить прямое управление коммуникационной аппаратурой, но требуется только возвратить допустимый маркер, если линия подключена.</span><span class="sxs-lookup"><span data-stu-id="bfa9c-110">If a call is active, the service provider typically opens the port itself to get direct control of the communications hardware, but is only required to return a valid handle if the line is connected.</span></span> <span data-ttu-id="bfa9c-111">Поставщик услуг открывает порт с использованием \_ \_ перекрывающегося значения флага файла, а затем настраивает порт с помощью параметров, заданных функцией [**линесетдевконфиг**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) .</span><span class="sxs-lookup"><span data-stu-id="bfa9c-111">The service provider opens the port using the FILE\_FLAG\_OVERLAPPED value and then configures the port using the settings specified by the [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) function.</span></span> <span data-ttu-id="bfa9c-112">Можно задать дополнительные параметры конфигурации для устройства с помощью функций связи с возвращенным маркером.</span><span class="sxs-lookup"><span data-stu-id="bfa9c-112">You can set additional configuration options for the device by using communications functions with the returned handle.</span></span>

<span data-ttu-id="bfa9c-113">Элемент **сздевиценаме** является строкой, завершающейся **нулем**, которая указывает имя порта связи, связанного со строкой, адресом или вызовом.</span><span class="sxs-lookup"><span data-stu-id="bfa9c-113">The **szDeviceName** member is a **null**-terminated string that specifies the name of the communications port associated with the line, address, or call.</span></span>

<span data-ttu-id="bfa9c-114">Если **хкомм** является допустимым маркером, его можно использовать при последующих вызовах файловых функций, таких как [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) и [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), для отправки и получения данных в вызове.</span><span class="sxs-lookup"><span data-stu-id="bfa9c-114">If **hComm** is a valid handle, you can use it in subsequent calls to file functions, such as [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) and [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), to send and receive data on the call.</span></span> <span data-ttu-id="bfa9c-115">Когда вы завершите использование порта связи и, прежде чем использовать функцию [**линедеаллокатекалл**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) для освобождения вызова, необходимо закрыть порт с помощью функции [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) .</span><span class="sxs-lookup"><span data-stu-id="bfa9c-115">When you are finished using the communications port and preferably before you use the [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) function to deallocate the call, you must close the port by using the [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) function.</span></span>

<span data-ttu-id="bfa9c-116">При использовании функций [**линежетдевконфиг**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) и [**линесетдевконфиг**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) некоторым поставщикам служб требуется, чтобы данные конфигурации для этого класса устройств имели следующий формат:</span><span class="sxs-lookup"><span data-stu-id="bfa9c-116">When using the [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) and [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) functions, some service providers require that the configuration data for this device class have the following format:</span></span>

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

<span data-ttu-id="bfa9c-117">Ниже приведены сведения о конфигурации устройства для использования с функциями [**линежетдевконфиг**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) и [**линесетдевконфиг**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) .</span><span class="sxs-lookup"><span data-stu-id="bfa9c-117">The following is device configuration information for use with the [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) and [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) functions.</span></span>

<dl> <dt>

<span data-ttu-id="bfa9c-118"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**двсизе**</span><span class="sxs-lookup"><span data-stu-id="bfa9c-118"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="bfa9c-119">Сумма размера структуры **девкфгхдр** и фактического размера структуры [**коммконфиг**](/windows/desktop/api/winbase/ns-winbase-commconfig) .</span><span class="sxs-lookup"><span data-stu-id="bfa9c-119">Sum of the size of the **DEVCFGHDR** structure and the actual size of the [**COMMCONFIG**](/windows/desktop/api/winbase/ns-winbase-commconfig) structure.</span></span>

</dd> <dt>

<span data-ttu-id="bfa9c-120"><span id="dwVersion"></span><span id="dwversion"></span><span id="DWVERSION"></span>**двверсион**</span><span class="sxs-lookup"><span data-stu-id="bfa9c-120"><span id="dwVersion"></span><span id="dwversion"></span><span id="DWVERSION"></span>**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="bfa9c-121">Номер версии структуры **Девконфиг** Unimodem.</span><span class="sxs-lookup"><span data-stu-id="bfa9c-121">Version number of the Unimodem **DevConfig** structure.</span></span> <span data-ttu-id="bfa9c-122">Этот член может иметь \_ версию мдмкфг (0x00010003).</span><span class="sxs-lookup"><span data-stu-id="bfa9c-122">This member can be MDMCFG\_VERSION (0x00010003).</span></span>

</dd> <dt>

<span data-ttu-id="bfa9c-123"><span id="fwOptions"></span><span id="fwoptions"></span><span id="FWOPTIONS"></span>**фвоптионс**</span><span class="sxs-lookup"><span data-stu-id="bfa9c-123"><span id="fwOptions"></span><span id="fwoptions"></span><span id="FWOPTIONS"></span>**fwOptions**</span></span>
</dt> <dd>

<span data-ttu-id="bfa9c-124">Флаги параметров, которые отображаются на странице параметров Unimodem.</span><span class="sxs-lookup"><span data-stu-id="bfa9c-124">Option flags that appear on the Unimodem Option page.</span></span> <span data-ttu-id="bfa9c-125">Этот элемент может быть сочетанием следующих значений:</span><span class="sxs-lookup"><span data-stu-id="bfa9c-125">This member can be a combination of these values:</span></span>

<dl> <dt>

<span data-ttu-id="bfa9c-126"><span id="TERMINAL_PRE__1_"></span><span id="terminal_pre__1_"></span>ТЕРМИНАЛ \_ до (1)</span><span class="sxs-lookup"><span data-stu-id="bfa9c-126"><span id="TERMINAL_PRE__1_"></span><span id="terminal_pre__1_"></span>TERMINAL\_PRE (1)</span></span>
</dt> <dd>

<span data-ttu-id="bfa9c-127">Отображает экран предварительного терминала.</span><span class="sxs-lookup"><span data-stu-id="bfa9c-127">Displays the pre-terminal screen.</span></span>

</dd> <dt>

<span data-ttu-id="bfa9c-128"><span id="TERMINAL_POST__2_"></span><span id="terminal_post__2_"></span>\_Запись терминала (2)</span><span class="sxs-lookup"><span data-stu-id="bfa9c-128"><span id="TERMINAL_POST__2_"></span><span id="terminal_post__2_"></span>TERMINAL\_POST (2)</span></span>
</dt> <dd>

<span data-ttu-id="bfa9c-129">Отображает экран после терминала.</span><span class="sxs-lookup"><span data-stu-id="bfa9c-129">Displays the post-terminal screen.</span></span>

</dd> <dt>

<span data-ttu-id="bfa9c-130"><span id="MANUAL_DIAL__4_"></span><span id="manual_dial__4_"></span>РУЧНОЙ \_ набор номера (4)</span><span class="sxs-lookup"><span data-stu-id="bfa9c-130"><span id="MANUAL_DIAL__4_"></span><span id="manual_dial__4_"></span>MANUAL\_DIAL (4)</span></span>
</dt> <dd>

<span data-ttu-id="bfa9c-131">Набирает телефон вручную, если это возможно.</span><span class="sxs-lookup"><span data-stu-id="bfa9c-131">Dials the phone manually, if capable of doing so.</span></span>

</dd> <dt>

<span data-ttu-id="bfa9c-132"><span id="LAUNCH_LIGHTS__8_"></span><span id="launch_lights__8_"></span>\_Индикаторы запуска (8)</span><span class="sxs-lookup"><span data-stu-id="bfa9c-132"><span id="LAUNCH_LIGHTS__8_"></span><span id="launch_lights__8_"></span>LAUNCH\_LIGHTS (8)</span></span>
</dt> <dd>

<span data-ttu-id="bfa9c-133">Отображает значок модема в области состояние панели задач.</span><span class="sxs-lookup"><span data-stu-id="bfa9c-133">Displays the modem icon in the status area of the taskbar.</span></span>

<span data-ttu-id="bfa9c-134">\_По умолчанию устанавливается только значение индикатора запуска</span><span class="sxs-lookup"><span data-stu-id="bfa9c-134">Only the LAUNCH\_LIGHTS value is set by default</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="bfa9c-135"><span id="wWaitBong"></span><span id="wwaitbong"></span><span id="WWAITBONG"></span>**вваитбонг**</span><span class="sxs-lookup"><span data-stu-id="bfa9c-135"><span id="wWaitBong"></span><span id="wwaitbong"></span><span id="WWAITBONG"></span>**wWaitBong**</span></span>
</dt> <dd>

<span data-ttu-id="bfa9c-136">Число секунд (с детализацией в две секунды) для замены ожидания гудка ($).</span><span class="sxs-lookup"><span data-stu-id="bfa9c-136">Number of seconds (in two seconds granularity) to replace the wait for credit tone ($).</span></span>

</dd> <dt>

<span data-ttu-id="bfa9c-137"><span id="Commconfig"></span><span id="commconfig"></span><span id="COMMCONFIG"></span>**коммконфиг**</span><span class="sxs-lookup"><span data-stu-id="bfa9c-137"><span id="Commconfig"></span><span id="commconfig"></span><span id="COMMCONFIG"></span>**Commconfig**</span></span>
</dt> <dd>

<span data-ttu-id="bfa9c-138">Структура [**коммконфиг**](/windows/desktop/api/winbase/ns-winbase-commconfig) , которую можно использовать с функциями настройки связи и модема.</span><span class="sxs-lookup"><span data-stu-id="bfa9c-138">[**COMMCONFIG**](/windows/desktop/api/winbase/ns-winbase-commconfig) structure that can be used with the communications and modem configuration functions.</span></span>

</dd> </dl>

 

 
