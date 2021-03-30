---
title: Метод Жетредиректаблеаддрессес класса Win32_TSSessionDirectory
description: Получает полный список доступных адресов DNS.
ms.assetid: 828079e7-472c-4428-97a0-2d5dedcdae91
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Жетредиректаблеаддрессес
- Службы удаленных рабочих столов метода Жетредиректаблеаддрессес, класс Win32_TSSessionDirectory
- Класс Win32_TSSessionDirectory службы удаленных рабочих столов, метод Жетредиректаблеаддрессес
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.GetRedirectableAddresses
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd5348c11b5f2aba442f7f13ef06488c6d849be3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071142"
---
# <a name="getredirectableaddresses-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="a0588-106">Метод Жетредиректаблеаддрессес \_ класса Win32 тссессиондиректори</span><span class="sxs-lookup"><span data-stu-id="a0588-106">GetRedirectableAddresses method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="a0588-107">Получает полный список доступных адресов DNS.</span><span class="sxs-lookup"><span data-stu-id="a0588-107">Obtains the entire list of DNS eligible addresses.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0588-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a0588-108">Syntax</span></span>


```mof
uint32 GetRedirectableAddresses(
  [in]  uint32 fTokenRedirection,
  [out] string IPAddresses[],
  [out] string AdapterNames[],
  [out] string NetConName[]
);
```



## <a name="parameters"></a><span data-ttu-id="a0588-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a0588-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0588-110">*фтокенредиректион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a0588-110">*fTokenRedirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0588-111">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a0588-111">Type: **uint32**</span></span>

<span data-ttu-id="a0588-112">Флаг, указывающий, следует ли использовать перенаправление токенов.</span><span class="sxs-lookup"><span data-stu-id="a0588-112">A flag that indicates whether token redirection should be used.</span></span>

</dd> <dt>

<span data-ttu-id="a0588-113">*Ipaddresses* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a0588-113">*IPAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a0588-114">Тип: **строка \[ \]**</span><span class="sxs-lookup"><span data-stu-id="a0588-114">Type: **string\[\]**</span></span>

<span data-ttu-id="a0588-115">Полный список IP-адресов, доступных для перенаправления.</span><span class="sxs-lookup"><span data-stu-id="a0588-115">The entire list of IP addresses that are available for redirection.</span></span>

</dd> <dt>

<span data-ttu-id="a0588-116">*Адаптернамес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a0588-116">*AdapterNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a0588-117">Тип: **строка \[ \]**</span><span class="sxs-lookup"><span data-stu-id="a0588-117">Type: **string\[\]**</span></span>

<span data-ttu-id="a0588-118">Список имен сетевых адаптеров, связанных с адресами, доступными для перенаправления.</span><span class="sxs-lookup"><span data-stu-id="a0588-118">The list of network adapter names that are associated with the addresses that are available for redirection.</span></span>

</dd> <dt>

<span data-ttu-id="a0588-119">*Нетконнаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a0588-119">*NetConName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a0588-120">Тип: **строка \[ \]**</span><span class="sxs-lookup"><span data-stu-id="a0588-120">Type: **string\[\]**</span></span>

<span data-ttu-id="a0588-121">Список имен сетевых подключений, связанных с адресами, доступными для перенаправления.</span><span class="sxs-lookup"><span data-stu-id="a0588-121">The list of network connection names that are associated with the addresses that are available for redirection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0588-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a0588-122">Return value</span></span>

<span data-ttu-id="a0588-123">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a0588-123">Type: **uint32**</span></span>

<span data-ttu-id="a0588-124">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="a0588-124">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="a0588-125">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="a0588-125">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0588-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a0588-126">Remarks</span></span>

<span data-ttu-id="a0588-127">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="a0588-127">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a0588-128">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="a0588-128">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="a0588-129">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="a0588-129">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a0588-130">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="a0588-130">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="a0588-131">Требования</span><span class="sxs-lookup"><span data-stu-id="a0588-131">Requirements</span></span>



| <span data-ttu-id="a0588-132">Требование</span><span class="sxs-lookup"><span data-stu-id="a0588-132">Requirement</span></span> | <span data-ttu-id="a0588-133">Значение</span><span class="sxs-lookup"><span data-stu-id="a0588-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0588-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a0588-134">Minimum supported client</span></span><br/> | <span data-ttu-id="a0588-135">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a0588-135">None supported</span></span><br/>                                                               |
| <span data-ttu-id="a0588-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a0588-136">Minimum supported server</span></span><br/> | <span data-ttu-id="a0588-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a0588-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a0588-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a0588-138">Namespace</span></span><br/>                | <span data-ttu-id="a0588-139">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="a0588-139">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="a0588-140">MOF</span><span class="sxs-lookup"><span data-stu-id="a0588-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a0588-141"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a0588-141"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="a0588-142">DLL</span><span class="sxs-lookup"><span data-stu-id="a0588-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0588-143"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0588-143"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0588-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a0588-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0588-145">**\_Тссессиондиректори Win32**</span><span class="sxs-lookup"><span data-stu-id="a0588-145">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

