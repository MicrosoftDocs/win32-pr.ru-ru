---
title: Метод Сеткуррентредиректаблеаддрессес класса Win32_TSSessionDirectory
description: Задает настроенный список доступных адресов DNS, которые могут использоваться для перенаправления.
ms.assetid: cad6a8a8-fdf1-406e-abeb-37acb396ac16
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сеткуррентредиректаблеаддрессес
- Службы удаленных рабочих столов метода Сеткуррентредиректаблеаддрессес, класс Win32_TSSessionDirectory
- Класс Win32_TSSessionDirectory службы удаленных рабочих столов, метод Сеткуррентредиректаблеаддрессес
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetCurrentRedirectableAddresses
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f43e70f8d108e908155b5db3e6800f4be26811c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415844"
---
# <a name="setcurrentredirectableaddresses-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="59427-106">Метод Сеткуррентредиректаблеаддрессес \_ класса Win32 тссессиондиректори</span><span class="sxs-lookup"><span data-stu-id="59427-106">SetCurrentRedirectableAddresses method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="59427-107">Метод **сеткуррентредиректаблеаддрессес** задает настроенный список доступных адресов DNS, которые могут использоваться для перенаправления.</span><span class="sxs-lookup"><span data-stu-id="59427-107">The **SetCurrentRedirectableAddresses** method sets the configured list of DNS eligible addresses that can be used for redirection.</span></span>

## <a name="syntax"></a><span data-ttu-id="59427-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="59427-108">Syntax</span></span>


```mof
uint32 SetCurrentRedirectableAddresses(
  [in] uint32 fTokenRedirection,
  [in] string IPAddresses[]
);
```



## <a name="parameters"></a><span data-ttu-id="59427-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="59427-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59427-110">*фтокенредиректион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="59427-110">*fTokenRedirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59427-111">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="59427-111">Type: **uint32**</span></span>

<span data-ttu-id="59427-112">Флаг, указывающий, следует ли использовать перенаправление токенов.</span><span class="sxs-lookup"><span data-stu-id="59427-112">A flag that indicates whether token redirection should be used.</span></span>

</dd> <dt>

<span data-ttu-id="59427-113">*Ipaddresses* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="59427-113">*IPAddresses* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59427-114">Тип: **строка \[ \]**</span><span class="sxs-lookup"><span data-stu-id="59427-114">Type: **string\[\]**</span></span>

<span data-ttu-id="59427-115">Массив строк, представляющий список IP-адресов, доступных DNS, которые могут использоваться для перенаправления.</span><span class="sxs-lookup"><span data-stu-id="59427-115">An array of strings that represents the list of DNS eligible IP addresses that can be used for redirection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59427-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="59427-116">Return value</span></span>

<span data-ttu-id="59427-117">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="59427-117">Type: **uint32**</span></span>

<span data-ttu-id="59427-118">Возвращает значение 0 в случае успешного выполнения; в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="59427-118">Returns 0 on success; otherwise, returns a WMI error code.</span></span> <span data-ttu-id="59427-119">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="59427-119">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="59427-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="59427-120">Remarks</span></span>

<span data-ttu-id="59427-121">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="59427-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="59427-122">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="59427-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="59427-123">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="59427-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="59427-124">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="59427-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="59427-125">Требования</span><span class="sxs-lookup"><span data-stu-id="59427-125">Requirements</span></span>



| <span data-ttu-id="59427-126">Требование</span><span class="sxs-lookup"><span data-stu-id="59427-126">Requirement</span></span> | <span data-ttu-id="59427-127">Значение</span><span class="sxs-lookup"><span data-stu-id="59427-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="59427-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="59427-128">Minimum supported client</span></span><br/> | <span data-ttu-id="59427-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="59427-129">None supported</span></span><br/>                                                               |
| <span data-ttu-id="59427-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="59427-130">Minimum supported server</span></span><br/> | <span data-ttu-id="59427-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="59427-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="59427-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="59427-132">Namespace</span></span><br/>                | <span data-ttu-id="59427-133">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="59427-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="59427-134">MOF</span><span class="sxs-lookup"><span data-stu-id="59427-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="59427-135"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="59427-135"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="59427-136">DLL</span><span class="sxs-lookup"><span data-stu-id="59427-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59427-137"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59427-137"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59427-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="59427-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59427-139">**\_Тссессиондиректори Win32**</span><span class="sxs-lookup"><span data-stu-id="59427-139">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

