---
title: Метод Селектнетворкадаптерип класса Win32_TSNetworkAdapterSetting
description: Выбирает сетевой адаптер на основе IP-адреса адаптера.
ms.assetid: 7f89fb83-8abe-421b-a48b-876c093e3a3d
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Селектнетворкадаптерип
- Службы удаленных рабочих столов метода Селектнетворкадаптерип, класс Win32_TSNetworkAdapterSetting
- Класс Win32_TSNetworkAdapterSetting службы удаленных рабочих столов, метод Селектнетворкадаптерип
topic_type:
- apiref
api_name:
- Win32_TSNetworkAdapterSetting.SelectNetworkAdapterIP
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9590bab26b3cda2e20a3dc74c5e201a2f7f86f94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681861"
---
# <a name="selectnetworkadapterip-method-of-the-win32_tsnetworkadaptersetting-class"></a><span data-ttu-id="25510-106">Метод Селектнетворкадаптерип \_ класса Win32 тснетворкадаптерсеттинг</span><span class="sxs-lookup"><span data-stu-id="25510-106">SelectNetworkAdapterIP method of the Win32\_TSNetworkAdapterSetting class</span></span>

<span data-ttu-id="25510-107">Выбирает сетевой адаптер на основе IP-адреса адаптера.</span><span class="sxs-lookup"><span data-stu-id="25510-107">Selects a network adapter based on the adapter's IP address.</span></span>

## <a name="syntax"></a><span data-ttu-id="25510-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="25510-108">Syntax</span></span>


```mof
uint32 SelectNetworkAdapterIP(
  [in] string NetworkAdapterIP
);
```



## <a name="parameters"></a><span data-ttu-id="25510-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="25510-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25510-110">*Нетворкадаптерип* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="25510-110">*NetworkAdapterIP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25510-111">IP-адрес устанавливаемого сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="25510-111">The IP address of the network adapter to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25510-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="25510-112">Return value</span></span>

<span data-ttu-id="25510-113">Возвращает нуль, если указанный IP-адрес является допустимым, и возвращает код ошибки WMI, если IP-адрес является недопустимым или не существует.</span><span class="sxs-lookup"><span data-stu-id="25510-113">Returns zero if the specified IP address is valid, and returns a WMI error code if the IP address is invalid or does not exist.</span></span> <span data-ttu-id="25510-114">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="25510-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="25510-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="25510-115">Remarks</span></span>

<span data-ttu-id="25510-116">IP-адрес сетевого адаптера можно получить, перечисляя свойства класса [**Win32 \_ тснетворкадаптерлистсеттинг**](win32-tsnetworkadapterlistsetting.md) .</span><span class="sxs-lookup"><span data-stu-id="25510-116">You can retrieve the IP address of a network adapter by enumerating the properties of the [**Win32\_TSNetworkAdapterListSetting**](win32-tsnetworkadapterlistsetting.md) class.</span></span>

<span data-ttu-id="25510-117">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="25510-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="25510-118">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="25510-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="25510-119">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="25510-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="25510-120">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="25510-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="25510-121">Требования</span><span class="sxs-lookup"><span data-stu-id="25510-121">Requirements</span></span>



| <span data-ttu-id="25510-122">Требование</span><span class="sxs-lookup"><span data-stu-id="25510-122">Requirement</span></span> | <span data-ttu-id="25510-123">Значение</span><span class="sxs-lookup"><span data-stu-id="25510-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="25510-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="25510-124">Minimum supported client</span></span><br/> | <span data-ttu-id="25510-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="25510-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="25510-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="25510-126">Minimum supported server</span></span><br/> | <span data-ttu-id="25510-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="25510-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="25510-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="25510-128">Namespace</span></span><br/>                | <span data-ttu-id="25510-129">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="25510-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="25510-130">MOF</span><span class="sxs-lookup"><span data-stu-id="25510-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="25510-131"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="25510-131"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="25510-132">DLL</span><span class="sxs-lookup"><span data-stu-id="25510-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25510-133"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25510-133"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25510-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="25510-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25510-135">**\_Тснетворкадаптерсеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="25510-135">**Win32\_TSNetworkAdapterSetting**</span></span>](win32-tsnetworkadaptersetting.md)
</dt> </dl>

 

