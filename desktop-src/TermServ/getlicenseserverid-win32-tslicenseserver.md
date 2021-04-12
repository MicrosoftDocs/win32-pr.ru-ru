---
title: Метод Жетлиценсесерверид класса Win32_TSLicenseServer
description: Возвращает идентификатор сервера лицензий удаленный рабочий стол, если сервер активирован в данный момент.
ms.assetid: 0eb2cf82-3632-4693-97d2-0cfa814d8c94
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Жетлиценсесерверид
- Службы удаленных рабочих столов метода Жетлиценсесерверид, класс Win32_TSLicenseServer
- Класс Win32_TSLicenseServer службы удаленных рабочих столов, метод Жетлиценсесерверид
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.GetLicenseServerId
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43a5883a5a52a0d111959e1f9fc1cbe9da5357d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415204"
---
# <a name="getlicenseserverid-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="00c12-106">Метод Жетлиценсесерверид \_ класса Win32 тслиценсесервер</span><span class="sxs-lookup"><span data-stu-id="00c12-106">GetLicenseServerId method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="00c12-107">Возвращает идентификатор сервера лицензий удаленный рабочий стол, если сервер активирован в данный момент.</span><span class="sxs-lookup"><span data-stu-id="00c12-107">Retrieves the Remote Desktop license server identifier if the server is currently activated.</span></span>

## <a name="syntax"></a><span data-ttu-id="00c12-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="00c12-108">Syntax</span></span>


```mof
uint32 GetLicenseServerId(
  [out] string sLicenseServerId
);
```



## <a name="parameters"></a><span data-ttu-id="00c12-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="00c12-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00c12-110">*слиценсесерверид* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="00c12-110">*sLicenseServerId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="00c12-111">Идентификатор сервера лицензирования удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="00c12-111">Remote Desktop license server identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00c12-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="00c12-112">Return value</span></span>

<span data-ttu-id="00c12-113">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="00c12-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="00c12-114">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="00c12-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="00c12-115">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="00c12-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="00c12-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="00c12-116">Remarks</span></span>

<span data-ttu-id="00c12-117">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="00c12-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="00c12-118">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="00c12-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="00c12-119">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="00c12-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="00c12-120">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="00c12-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="00c12-121">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="00c12-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="00c12-122">Требования</span><span class="sxs-lookup"><span data-stu-id="00c12-122">Requirements</span></span>



| <span data-ttu-id="00c12-123">Требование</span><span class="sxs-lookup"><span data-stu-id="00c12-123">Requirement</span></span> | <span data-ttu-id="00c12-124">Значение</span><span class="sxs-lookup"><span data-stu-id="00c12-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="00c12-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="00c12-125">Minimum supported client</span></span><br/> | <span data-ttu-id="00c12-126">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="00c12-126">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="00c12-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="00c12-127">Minimum supported server</span></span><br/> | <span data-ttu-id="00c12-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="00c12-128">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="00c12-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="00c12-129">Namespace</span></span><br/>                | <span data-ttu-id="00c12-130">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="00c12-130">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="00c12-131">MOF</span><span class="sxs-lookup"><span data-stu-id="00c12-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="00c12-132"><dt>Тлсвмипров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="00c12-132"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="00c12-133">DLL</span><span class="sxs-lookup"><span data-stu-id="00c12-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00c12-134"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00c12-134"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00c12-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="00c12-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00c12-136">**\_Тслиценсесервер Win32**</span><span class="sxs-lookup"><span data-stu-id="00c12-136">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

