---
title: Метод Сетнетворкадаптерланаид класса Win32_TSNetworkAdapterSetting
description: Указывает номер локальной сетевой карты (LANA) для установки сетевого адаптера.
ms.assetid: a12c7f06-4ecf-40bd-98c5-a2583dd1754a
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетнетворкадаптерланаид
- Службы удаленных рабочих столов метода Сетнетворкадаптерланаид, класс Win32_TSNetworkAdapterSetting
- Класс Win32_TSNetworkAdapterSetting службы удаленных рабочих столов, метод Сетнетворкадаптерланаид
topic_type:
- apiref
api_name:
- Win32_TSNetworkAdapterSetting.SetNetworkAdapterLanaID
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00675ae6378041e6c06b82a7de3c1ccf27620f4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803772"
---
# <a name="setnetworkadapterlanaid-method-of-the-win32_tsnetworkadaptersetting-class"></a><span data-ttu-id="0b936-106">Метод Сетнетворкадаптерланаид \_ класса Win32 тснетворкадаптерсеттинг</span><span class="sxs-lookup"><span data-stu-id="0b936-106">SetNetworkAdapterLanaID method of the Win32\_TSNetworkAdapterSetting class</span></span>

<span data-ttu-id="0b936-107">Метод **сетнетворкадаптерланаид** указывает номер локальной сети (Lana) сетевого адаптера, который нужно установить.</span><span class="sxs-lookup"><span data-stu-id="0b936-107">The **SetNetworkAdapterLanaID** method specifies the Local Area Network Adapter (LANA) number of the network adapter to set.</span></span> <span data-ttu-id="0b936-108">Если указанный идентификатор LANA недопустим или не существует, возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="0b936-108">If the LANA ID specified is not valid or does not exist, an error is returned.</span></span> <span data-ttu-id="0b936-109">Список доступных идентификаторов LANA можно получить, перечисляя свойство **девицеидлист** в классе [**Win32 \_ тснетворкадаптерсеттинг**](win32-tsnetworkadaptersetting.md) .</span><span class="sxs-lookup"><span data-stu-id="0b936-109">The available list of LANA IDs is obtained by enumerating the property **DeviceIDList** in the [**Win32\_TSNetworkAdapterSetting**](win32-tsnetworkadaptersetting.md) class.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b936-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0b936-110">Syntax</span></span>


```mof
uint32 SetNetworkAdapterLanaID(
  [in] uint32 NetworkAdapterLanaID
);
```



## <a name="parameters"></a><span data-ttu-id="0b936-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="0b936-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b936-112">*Нетворкадаптерланаид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0b936-112">*NetworkAdapterLanaID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b936-113">Номер LANA устанавливаемого сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="0b936-113">LANA number of the network adapter to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b936-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0b936-114">Return value</span></span>

<span data-ttu-id="0b936-115">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="0b936-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="0b936-116">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="0b936-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b936-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0b936-117">Remarks</span></span>

<span data-ttu-id="0b936-118">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="0b936-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="0b936-119">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="0b936-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="0b936-120">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="0b936-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="0b936-121">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="0b936-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="0b936-122">Требования</span><span class="sxs-lookup"><span data-stu-id="0b936-122">Requirements</span></span>



| <span data-ttu-id="0b936-123">Требование</span><span class="sxs-lookup"><span data-stu-id="0b936-123">Requirement</span></span> | <span data-ttu-id="0b936-124">Значение</span><span class="sxs-lookup"><span data-stu-id="0b936-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b936-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0b936-125">Minimum supported client</span></span><br/> | <span data-ttu-id="0b936-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0b936-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0b936-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0b936-127">Minimum supported server</span></span><br/> | <span data-ttu-id="0b936-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0b936-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0b936-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0b936-129">Namespace</span></span><br/>                | <span data-ttu-id="0b936-130">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="0b936-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="0b936-131">MOF</span><span class="sxs-lookup"><span data-stu-id="0b936-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0b936-132"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0b936-132"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="0b936-133">DLL</span><span class="sxs-lookup"><span data-stu-id="0b936-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b936-134"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b936-134"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b936-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0b936-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b936-136">**\_Тснетворкадаптерсеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="0b936-136">**Win32\_TSNetworkAdapterSetting**</span></span>](win32-tsnetworkadaptersetting.md)
</dt> </dl>

 

