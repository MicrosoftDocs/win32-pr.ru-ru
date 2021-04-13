---
title: Метод Жеткуррентредиректаблеаддрессес класса Win32_TSSessionDirectory
description: Получает список доступных адресов DNS, которые можно использовать для перенаправления.
ms.assetid: 79f35d8f-b5f9-4b0f-bb7d-0d1ee3f02346
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Жеткуррентредиректаблеаддрессес
- Службы удаленных рабочих столов метода Жеткуррентредиректаблеаддрессес, класс Win32_TSSessionDirectory
- Класс Win32_TSSessionDirectory службы удаленных рабочих столов, метод Жеткуррентредиректаблеаддрессес
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.GetCurrentRedirectableAddresses
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e6b4a859c77f449fb5a8f436be6e18c058ca59f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492786"
---
# <a name="getcurrentredirectableaddresses-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="e3b87-106">Метод Жеткуррентредиректаблеаддрессес \_ класса Win32 тссессиондиректори</span><span class="sxs-lookup"><span data-stu-id="e3b87-106">GetCurrentRedirectableAddresses method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="e3b87-107">Получает список доступных адресов DNS, которые можно использовать для перенаправления.</span><span class="sxs-lookup"><span data-stu-id="e3b87-107">Obtains the currently configured list of DNS eligible addresses that can be used for redirection.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3b87-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e3b87-108">Syntax</span></span>


```mof
uint32 GetCurrentRedirectableAddresses(
  [out] uint32 fTokenRedirection,
  [out] string IPAddresses[]
);
```



## <a name="parameters"></a><span data-ttu-id="e3b87-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="e3b87-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3b87-110">*фтокенредиректион* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e3b87-110">*fTokenRedirection* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e3b87-111">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e3b87-111">Type: **uint32**</span></span>

<span data-ttu-id="e3b87-112">Флаг, указывающий, следует ли использовать перенаправление токенов.</span><span class="sxs-lookup"><span data-stu-id="e3b87-112">A flag that indicates whether token redirection should be used.</span></span>

</dd> <dt>

<span data-ttu-id="e3b87-113">*Ipaddresses* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e3b87-113">*IPAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e3b87-114">Тип: **строка \[ \]**</span><span class="sxs-lookup"><span data-stu-id="e3b87-114">Type: **string\[\]**</span></span>

<span data-ttu-id="e3b87-115">Массив настроенных в настоящее время IP-адресов DNS, которые можно использовать для перенаправления.</span><span class="sxs-lookup"><span data-stu-id="e3b87-115">An array of the currently configured DNS eligible IP addresses that can be used for redirection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3b87-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e3b87-116">Return value</span></span>

<span data-ttu-id="e3b87-117">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e3b87-117">Type: **uint32**</span></span>

<span data-ttu-id="e3b87-118">Возвращает значение 0 в случае успешного выполнения; в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="e3b87-118">Returns 0 on success; otherwise, returns a WMI error code.</span></span> <span data-ttu-id="e3b87-119">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="e3b87-119">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3b87-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e3b87-120">Remarks</span></span>

<span data-ttu-id="e3b87-121">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="e3b87-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e3b87-122">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="e3b87-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="e3b87-123">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="e3b87-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e3b87-124">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="e3b87-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="e3b87-125">Требования</span><span class="sxs-lookup"><span data-stu-id="e3b87-125">Requirements</span></span>



| <span data-ttu-id="e3b87-126">Требование</span><span class="sxs-lookup"><span data-stu-id="e3b87-126">Requirement</span></span> | <span data-ttu-id="e3b87-127">Значение</span><span class="sxs-lookup"><span data-stu-id="e3b87-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3b87-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e3b87-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e3b87-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e3b87-129">None supported</span></span><br/>                                                               |
| <span data-ttu-id="e3b87-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e3b87-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e3b87-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e3b87-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e3b87-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e3b87-132">Namespace</span></span><br/>                | <span data-ttu-id="e3b87-133">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="e3b87-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="e3b87-134">MOF</span><span class="sxs-lookup"><span data-stu-id="e3b87-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e3b87-135"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e3b87-135"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="e3b87-136">DLL</span><span class="sxs-lookup"><span data-stu-id="e3b87-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3b87-137"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3b87-137"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3b87-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e3b87-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3b87-139">**\_Тссессиондиректори Win32**</span><span class="sxs-lookup"><span data-stu-id="e3b87-139">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

