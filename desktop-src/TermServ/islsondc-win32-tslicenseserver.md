---
title: Метод Ислсондк класса Win32_TSLicenseServer
description: Получает значение, указывающее, установлена ли на контроллере домена удаленный рабочий стол лицензирования (лицензирование удаленных рабочих столов).
ms.assetid: 43345dc8-c8b6-4c41-b26d-781293d07516
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Ислсондк
- Службы удаленных рабочих столов метода Ислсондк, класс Win32_TSLicenseServer
- Класс Win32_TSLicenseServer службы удаленных рабочих столов, метод Ислсондк
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSonDC
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03ddbf01615903150ffa8f97fca88cfcf7fda937
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988853"
---
# <a name="islsondc-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="5a860-106">Метод Ислсондк \_ класса Win32 тслиценсесервер</span><span class="sxs-lookup"><span data-stu-id="5a860-106">IsLSonDC method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="5a860-107">Получает значение, указывающее, установлена ли на контроллере домена удаленный рабочий стол лицензирования (лицензирование удаленных рабочих столов).</span><span class="sxs-lookup"><span data-stu-id="5a860-107">Retrieves whether Remote Desktop Licensing (RD Licensing) is installed on a domain controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a860-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5a860-108">Syntax</span></span>


```mof
uint32 IsLSonDC(
  [out] boolean OnDC
);
```



## <a name="parameters"></a><span data-ttu-id="5a860-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="5a860-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a860-110">*Ондк* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5a860-110">*OnDC* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a860-111">Логическое значение, указывающее, установлена ли на контроллере домена Служба лицензирования удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="5a860-111">Boolean value that indicates whether RD Licensing is installed on a domain controller.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a860-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5a860-112">Return value</span></span>

<span data-ttu-id="5a860-113">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="5a860-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="5a860-114">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="5a860-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="5a860-115">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="5a860-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5a860-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5a860-116">Remarks</span></span>

<span data-ttu-id="5a860-117">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="5a860-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="5a860-118">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="5a860-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5a860-119">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="5a860-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="5a860-120">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="5a860-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5a860-121">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="5a860-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="5a860-122">Требования</span><span class="sxs-lookup"><span data-stu-id="5a860-122">Requirements</span></span>



| <span data-ttu-id="5a860-123">Требование</span><span class="sxs-lookup"><span data-stu-id="5a860-123">Requirement</span></span> | <span data-ttu-id="5a860-124">Значение</span><span class="sxs-lookup"><span data-stu-id="5a860-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a860-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5a860-125">Minimum supported client</span></span><br/> | <span data-ttu-id="5a860-126">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="5a860-126">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="5a860-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5a860-127">Minimum supported server</span></span><br/> | <span data-ttu-id="5a860-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5a860-128">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="5a860-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="5a860-129">Namespace</span></span><br/>                | <span data-ttu-id="5a860-130">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="5a860-130">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="5a860-131">MOF</span><span class="sxs-lookup"><span data-stu-id="5a860-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5a860-132"><dt>Тлсвмипров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5a860-132"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="5a860-133">DLL</span><span class="sxs-lookup"><span data-stu-id="5a860-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a860-134"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a860-134"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a860-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5a860-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a860-136">**\_Тслиценсесервер Win32**</span><span class="sxs-lookup"><span data-stu-id="5a860-136">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

