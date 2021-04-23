---
title: Команда MCI_SYSINFO (Ммсистем. h)
description: Команда MCI \_ сисинфо извлекает сведения об устройствах MCI.
ms.assetid: 605efd25-8849-42aa-99fd-b36b6fd2c7b7
keywords:
- MCI_SYSINFO команды мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_SYSINFO
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e722625449893771726a83738c3b0d7bc8bc523c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988764"
---
# <a name="mci_sysinfo-command"></a><span data-ttu-id="2f072-104">\_Команда MCI сисинфо</span><span class="sxs-lookup"><span data-stu-id="2f072-104">MCI\_SYSINFO command</span></span>

<span data-ttu-id="2f072-105">Команда MCI \_ сисинфо извлекает сведения об устройствах MCI.</span><span class="sxs-lookup"><span data-stu-id="2f072-105">The MCI\_SYSINFO command retrieves information about MCI devices.</span></span> <span data-ttu-id="2f072-106">MCI поддерживает эту команду напрямую, а не передает ее на устройство.</span><span class="sxs-lookup"><span data-stu-id="2f072-106">MCI supports this command directly rather than passing it to the device.</span></span> <span data-ttu-id="2f072-107">С помощью этой команды можно использовать любое приложение MCI.</span><span class="sxs-lookup"><span data-stu-id="2f072-107">Any MCI application can use this command.</span></span> <span data-ttu-id="2f072-108">Строковые данные возвращаются в предоставленном приложением буфере, на который указывает элемент **лпстрретурн** структуры, идентифицируемой *лпсисинфо*.</span><span class="sxs-lookup"><span data-stu-id="2f072-108">String information is returned in the application-supplied buffer pointed to by the **lpstrReturn** member of the structure identified by *lpSysInfo*.</span></span> <span data-ttu-id="2f072-109">Числовые данные возвращаются в виде значения **DWORD** , помещенного в буфер, предоставляемый приложением.</span><span class="sxs-lookup"><span data-stu-id="2f072-109">Numeric information is returned as a **DWORD** value placed in the application-supplied buffer.</span></span> <span data-ttu-id="2f072-110">Элемент **двретсизе** указывает длину буфера.</span><span class="sxs-lookup"><span data-stu-id="2f072-110">The **dwRetSize** member specifies the buffer length.</span></span>

<span data-ttu-id="2f072-111">Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="2f072-111">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SYSINFO, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_SYSINFO_PARMS) lpSysInfo
);
```



## <a name="parameters"></a><span data-ttu-id="2f072-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="2f072-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f072-113"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*вдевицеид*</span><span class="sxs-lookup"><span data-stu-id="2f072-113"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="2f072-114">Идентификатор устройства MCI, который должен получить командное сообщение.</span><span class="sxs-lookup"><span data-stu-id="2f072-114">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="2f072-115"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="2f072-115"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="2f072-116">Один или несколько из следующих стандартных флагов и отдельных команд:</span><span class="sxs-lookup"><span data-stu-id="2f072-116">One or more of the following standard and command-specific flags:</span></span>

</dd> <dt>

<span data-ttu-id="2f072-117"><span id="MCI_SYSINFO_INSTALLNAME"></span><span id="mci_sysinfo_installname"></span>\_ИНСТАЛЛНАМЕ MCI сисинфо \_</span><span class="sxs-lookup"><span data-stu-id="2f072-117"><span id="MCI_SYSINFO_INSTALLNAME"></span><span id="mci_sysinfo_installname"></span>MCI\_SYSINFO\_INSTALLNAME</span></span>
</dt> <dd>

<span data-ttu-id="2f072-118">Получает имя (указанное в реестре или файле SYSTEM.INI), используемое для установки устройства.</span><span class="sxs-lookup"><span data-stu-id="2f072-118">Obtains the name (listed in the registry or the SYSTEM.INI file) used to install the device.</span></span>

</dd> <dt>

<span data-ttu-id="2f072-119"><span id="MCI_SYSINFO_NAME"></span><span id="mci_sysinfo_name"></span>\_имя СИСИНФО \_ MCI</span><span class="sxs-lookup"><span data-stu-id="2f072-119"><span id="MCI_SYSINFO_NAME"></span><span id="mci_sysinfo_name"></span>MCI\_SYSINFO\_NAME</span></span>
</dt> <dd>

<span data-ttu-id="2f072-120">Получает имя устройства, соответствующее номеру устройства, указанному в элементе **двнумбер** структуры, определенной параметром **лпсисинфо**.</span><span class="sxs-lookup"><span data-stu-id="2f072-120">Obtains a device name corresponding to the device number specified in the **dwNumber** member of the structure identified by **lpSysInfo**.</span></span> <span data-ttu-id="2f072-121">Если установлен \_ \_ флаг открытия MCI сисинфо, то MCI возвращает имена открытых устройств.</span><span class="sxs-lookup"><span data-stu-id="2f072-121">If the MCI\_SYSINFO\_OPEN flag is set, MCI returns the names of open devices.</span></span>

</dd> <dt>

<span data-ttu-id="2f072-122"><span id="MCI_SYSINFO_OPEN"></span><span id="mci_sysinfo_open"></span>\_Открытие MCI сисинфо \_</span><span class="sxs-lookup"><span data-stu-id="2f072-122"><span id="MCI_SYSINFO_OPEN"></span><span id="mci_sysinfo_open"></span>MCI\_SYSINFO\_OPEN</span></span>
</dt> <dd>

<span data-ttu-id="2f072-123">Получает количество или имя открытых устройств.</span><span class="sxs-lookup"><span data-stu-id="2f072-123">Obtains the quantity or name of open devices.</span></span>

</dd> <dt>

<span data-ttu-id="2f072-124"><span id="MCI_SYSINFO_QUANTITY"></span><span id="mci_sysinfo_quantity"></span>\_количество СИСИНФО \_ MCI</span><span class="sxs-lookup"><span data-stu-id="2f072-124"><span id="MCI_SYSINFO_QUANTITY"></span><span id="mci_sysinfo_quantity"></span>MCI\_SYSINFO\_QUANTITY</span></span>
</dt> <dd>

<span data-ttu-id="2f072-125">Получает число устройств указанного типа, перечисленных в реестре или в \[ \] разделе mci файла SYSTEM.INI.</span><span class="sxs-lookup"><span data-stu-id="2f072-125">Obtains the number of devices of the specified type that are listed in the registry or the \[mci\] section of the SYSTEM.INI file.</span></span> <span data-ttu-id="2f072-126">Если установлен \_ \_ флаг открытия MCI сисинфо, возвращается число открытых устройств.</span><span class="sxs-lookup"><span data-stu-id="2f072-126">If the MCI\_SYSINFO\_OPEN flag is set, the number of open devices is returned.</span></span>

</dd> <dt>

<span data-ttu-id="2f072-127"><span id="lpSysInfo"></span><span id="lpsysinfo"></span><span id="LPSYSINFO"></span>*лпсисинфо*</span><span class="sxs-lookup"><span data-stu-id="2f072-127"><span id="lpSysInfo"></span><span id="lpsysinfo"></span><span id="LPSYSINFO"></span>*lpSysInfo*</span></span>
</dt> <dd>

<span data-ttu-id="2f072-128">Указатель на структуру [**\_ \_ пармс MCI сисинфо**](mci-sysinfo-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="2f072-128">Pointer to an [**MCI\_SYSINFO\_PARMS**](mci-sysinfo-parms.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f072-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2f072-129">Return Value</span></span>

<span data-ttu-id="2f072-130">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="2f072-130">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f072-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2f072-131">Remarks</span></span>

<span data-ttu-id="2f072-132">Элемент **вдевицетипе** структуры, идентифицируемой *лпсисинфо* , используется для указания типа устройства запроса.</span><span class="sxs-lookup"><span data-stu-id="2f072-132">The **wDeviceType** member of the structure identified by *lpSysInfo* is used to indicate the device type of the query.</span></span> <span data-ttu-id="2f072-133">Если для параметра *вдевицеид* задано значение MCI \_ All \_ Device \_ ID, то переопределение значения **вдевицетипе**.</span><span class="sxs-lookup"><span data-stu-id="2f072-133">If the *wDeviceID* parameter is set to MCI\_ALL\_DEVICE\_ID, it overrides the value of **wDeviceType**.</span></span> <span data-ttu-id="2f072-134">Список типов устройств см. в разделе [типы устройств MCI](mci-device-types.md).</span><span class="sxs-lookup"><span data-stu-id="2f072-134">For a list of device types, see [MCI Device Types](mci-device-types.md).</span></span>

<span data-ttu-id="2f072-135">Целочисленные возвращаемые значения — это значения **DWORD** , возвращаемые в буфер, на который указывает элемент **лпстрретурн** структуры, идентифицируемой *лпсисинфо*.</span><span class="sxs-lookup"><span data-stu-id="2f072-135">Integer return values are **DWORD** values returned in the buffer pointed to by the **lpstrReturn** member of the structure identified by *lpSysInfo*.</span></span>

<span data-ttu-id="2f072-136">Возвращаемые строковые значения — это строки, заканчивающиеся нулем, возвращаемые в буфер, на который указывает элемент **лпстрретурн** структуры, идентифицируемой *лпсисинфо*.</span><span class="sxs-lookup"><span data-stu-id="2f072-136">String return values are null-terminated strings returned in the buffer pointed to by the **lpstrReturn** member of the structure identified by *lpSysInfo*.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f072-137">Требования</span><span class="sxs-lookup"><span data-stu-id="2f072-137">Requirements</span></span>



| <span data-ttu-id="2f072-138">Требование</span><span class="sxs-lookup"><span data-stu-id="2f072-138">Requirement</span></span> | <span data-ttu-id="2f072-139">Значение</span><span class="sxs-lookup"><span data-stu-id="2f072-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f072-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2f072-140">Minimum supported client</span></span><br/> | <span data-ttu-id="2f072-141">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2f072-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="2f072-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2f072-142">Minimum supported server</span></span><br/> | <span data-ttu-id="2f072-143">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2f072-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="2f072-144">Заголовок</span><span class="sxs-lookup"><span data-stu-id="2f072-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f072-145"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2f072-145"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f072-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2f072-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f072-147">MCI</span><span class="sxs-lookup"><span data-stu-id="2f072-147">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="2f072-148">Команды MCI</span><span class="sxs-lookup"><span data-stu-id="2f072-148">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

