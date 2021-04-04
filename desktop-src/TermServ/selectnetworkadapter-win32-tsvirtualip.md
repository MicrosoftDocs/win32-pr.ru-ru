---
title: Метод Селектнетворкадаптер класса Win32_TSVirtualIP
description: Задает MAC-адрес сетевого адаптера, используемого для виртуализации IP.
ms.assetid: ad67445c-6a8b-4980-997a-56aceb70965f
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Селектнетворкадаптер
- Службы удаленных рабочих столов метода Селектнетворкадаптер, класс Win32_TSVirtualIP
- Класс Win32_TSVirtualIP службы удаленных рабочих столов, метод Селектнетворкадаптер
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SelectNetworkAdapter
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3a362bea1a5cacbfd727f23504f19164c79ce65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988573"
---
# <a name="selectnetworkadapter-method-of-the-win32_tsvirtualip-class"></a><span data-ttu-id="131ff-106">Метод Селектнетворкадаптер \_ класса Win32 тсвиртуалип</span><span class="sxs-lookup"><span data-stu-id="131ff-106">SelectNetworkAdapter method of the Win32\_TSVirtualIP class</span></span>

<span data-ttu-id="131ff-107">Задает MAC-адрес сетевого адаптера, используемого для виртуализации IP.</span><span class="sxs-lookup"><span data-stu-id="131ff-107">Sets the MAC address of the network adapter to use for IP virtualization.</span></span>

## <a name="syntax"></a><span data-ttu-id="131ff-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="131ff-108">Syntax</span></span>


```mof
uint32 SelectNetworkAdapter(
  [in] string NetworkAdapterMacAddress
);
```



## <a name="parameters"></a><span data-ttu-id="131ff-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="131ff-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="131ff-110">*Нетворкадаптермакаддресс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="131ff-110">*NetworkAdapterMacAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="131ff-111">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="131ff-111">Type: **string**</span></span>

<span data-ttu-id="131ff-112">Указывает MAC-адрес сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="131ff-112">Specifies the MAC address of the network adapter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="131ff-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="131ff-113">Return value</span></span>

<span data-ttu-id="131ff-114">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="131ff-114">Type: **uint32**</span></span>

<span data-ttu-id="131ff-115">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="131ff-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="131ff-116">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="131ff-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

<span data-ttu-id="131ff-117">Если MAC-адрес является недопустимым или не существует, или если используется режим виртуализации IP для каждого сеанса, возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="131ff-117">If the MAC address is invalid or does not exist, or if the IP virtualization mode is per-session, an error is returned.</span></span>

<span data-ttu-id="131ff-118">Метод возвращает ошибку, если параметр находится в разделе Управление групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="131ff-118">The method returns an error if the setting is under group policy control.</span></span>

## <a name="requirements"></a><span data-ttu-id="131ff-119">Требования</span><span class="sxs-lookup"><span data-stu-id="131ff-119">Requirements</span></span>



| <span data-ttu-id="131ff-120">Требование</span><span class="sxs-lookup"><span data-stu-id="131ff-120">Requirement</span></span> | <span data-ttu-id="131ff-121">Значение</span><span class="sxs-lookup"><span data-stu-id="131ff-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="131ff-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="131ff-122">Minimum supported client</span></span><br/> | <span data-ttu-id="131ff-123">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="131ff-123">None supported</span></span><br/>                                                               |
| <span data-ttu-id="131ff-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="131ff-124">Minimum supported server</span></span><br/> | <span data-ttu-id="131ff-125">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="131ff-125">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="131ff-126">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="131ff-126">Namespace</span></span><br/>                | <span data-ttu-id="131ff-127">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="131ff-127">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="131ff-128">MOF</span><span class="sxs-lookup"><span data-stu-id="131ff-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="131ff-129"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="131ff-129"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="131ff-130">DLL</span><span class="sxs-lookup"><span data-stu-id="131ff-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="131ff-131"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="131ff-131"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="131ff-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="131ff-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="131ff-133">**\_Тсвиртуалип Win32**</span><span class="sxs-lookup"><span data-stu-id="131ff-133">**Win32\_TSVirtualIP**</span></span>](win32-tsvirtualip.md)
</dt> </dl>

 

 





