---
title: Метод Деактиватесервер класса Win32_TSLicenseServer
description: Деактивирует сервер лицензий удаленный рабочий стол, используя код подтверждения, полученный по телефону.
ms.assetid: 84e069b7-9a4f-4843-b656-839f936ac727
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Деактиватесервер
- Службы удаленных рабочих столов метода Деактиватесервер, класс Win32_TSLicenseServer
- Класс Win32_TSLicenseServer службы удаленных рабочих столов, метод Деактиватесервер
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.DeactivateServer
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23b851a8d8049c9194bce163afc4b7bad5d4aa15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988286"
---
# <a name="deactivateserver-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="06fc4-106">Метод Деактиватесервер \_ класса Win32 тслиценсесервер</span><span class="sxs-lookup"><span data-stu-id="06fc4-106">DeactivateServer method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="06fc4-107">Деактивирует сервер лицензий удаленный рабочий стол, используя код подтверждения, полученный по телефону.</span><span class="sxs-lookup"><span data-stu-id="06fc4-107">Deactivates the Remote Desktop license server by using a confirmation code that is received over the phone.</span></span>

## <a name="syntax"></a><span data-ttu-id="06fc4-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="06fc4-108">Syntax</span></span>


```mof
uint32 DeactivateServer(
  [in]  string sConfirmCode,
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a><span data-ttu-id="06fc4-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="06fc4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06fc4-110">*сконфирмкоде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="06fc4-110">*sConfirmCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06fc4-111">Код подтверждения.</span><span class="sxs-lookup"><span data-stu-id="06fc4-111">Confirmation code.</span></span>

</dd> <dt>

<span data-ttu-id="06fc4-112">*ActivationStatus* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="06fc4-112">*ActivationStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="06fc4-113">Возвращенное состояние активации может быть одним из следующих.</span><span class="sxs-lookup"><span data-stu-id="06fc4-113">The activation status returned can be one of the following.</span></span>

<dt>

<span data-ttu-id="06fc4-114">0</span><span class="sxs-lookup"><span data-stu-id="06fc4-114">0</span></span>
</dt> <dd>

<span data-ttu-id="06fc4-115">Сервер лицензий удаленный рабочий стол активирован.</span><span class="sxs-lookup"><span data-stu-id="06fc4-115">The Remote Desktop license server is activated.</span></span>

</dd> <dt>

<span data-ttu-id="06fc4-116">1</span><span class="sxs-lookup"><span data-stu-id="06fc4-116">1</span></span>
</dt> <dd>

<span data-ttu-id="06fc4-117">Сервер лицензирования удаленный рабочий стол не активирован.</span><span class="sxs-lookup"><span data-stu-id="06fc4-117">The Remote Desktop license server is not activated.</span></span>

</dd> <dt>

<span data-ttu-id="06fc4-118">2</span><span class="sxs-lookup"><span data-stu-id="06fc4-118">2</span></span>
</dt> <dd>

<span data-ttu-id="06fc4-119">Произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="06fc4-119">An unknown error occurred.</span></span> <span data-ttu-id="06fc4-120">Неизвестно, активирован ли сервер лицензий службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="06fc4-120">It is not known whether the Remote Desktop Services license server is activated.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06fc4-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="06fc4-121">Return value</span></span>

<span data-ttu-id="06fc4-122">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="06fc4-122">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="06fc4-123">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="06fc4-123">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="06fc4-124">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="06fc4-124">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="06fc4-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="06fc4-125">Remarks</span></span>

<span data-ttu-id="06fc4-126">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="06fc4-126">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="06fc4-127">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="06fc4-127">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="06fc4-128">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="06fc4-128">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="06fc4-129">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="06fc4-129">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="06fc4-130">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="06fc4-130">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="06fc4-131">Требования</span><span class="sxs-lookup"><span data-stu-id="06fc4-131">Requirements</span></span>



| <span data-ttu-id="06fc4-132">Требование</span><span class="sxs-lookup"><span data-stu-id="06fc4-132">Requirement</span></span> | <span data-ttu-id="06fc4-133">Значение</span><span class="sxs-lookup"><span data-stu-id="06fc4-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="06fc4-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="06fc4-134">Minimum supported client</span></span><br/> | <span data-ttu-id="06fc4-135">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="06fc4-135">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="06fc4-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="06fc4-136">Minimum supported server</span></span><br/> | <span data-ttu-id="06fc4-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="06fc4-137">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="06fc4-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="06fc4-138">Namespace</span></span><br/>                | <span data-ttu-id="06fc4-139">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="06fc4-139">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="06fc4-140">MOF</span><span class="sxs-lookup"><span data-stu-id="06fc4-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="06fc4-141"><dt>Тлсвмипров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="06fc4-141"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="06fc4-142">DLL</span><span class="sxs-lookup"><span data-stu-id="06fc4-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06fc4-143"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06fc4-143"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06fc4-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="06fc4-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06fc4-145">**\_Тслиценсесервер Win32**</span><span class="sxs-lookup"><span data-stu-id="06fc4-145">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

