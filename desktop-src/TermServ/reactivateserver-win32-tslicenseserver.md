---
title: Метод Реактиватесервер класса Win32_TSLicenseServer
description: Повторно активирует сервер лицензий удаленный рабочий стол, используя новый идентификатор, полученный по телефону или через Интернет.
ms.assetid: dd9ff938-a683-4f60-b7cc-7580892953b6
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Реактиватесервер
- Службы удаленных рабочих столов метода Реактиватесервер, класс Win32_TSLicenseServer
- Класс Win32_TSLicenseServer службы удаленных рабочих столов, метод Реактиватесервер
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.ReactivateServer
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50e84eb0bed0b52ad463fce50ce334d6c8eb8d80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490602"
---
# <a name="reactivateserver-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="f3d95-106">Метод Реактиватесервер \_ класса Win32 тслиценсесервер</span><span class="sxs-lookup"><span data-stu-id="f3d95-106">ReactivateServer method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="f3d95-107">Повторно активирует сервер лицензий удаленный рабочий стол, используя новый идентификатор, полученный по телефону или через Интернет.</span><span class="sxs-lookup"><span data-stu-id="f3d95-107">Reactivates the Remote Desktop license server by using a new identifier that was obtained over the phone or the Internet.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3d95-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f3d95-108">Syntax</span></span>


```mof
uint32 ReactivateServer(
  [in]  string sNewLicenseServerId,
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a><span data-ttu-id="f3d95-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f3d95-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3d95-110">*сневлиценсесерверид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f3d95-110">*sNewLicenseServerId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3d95-111">Идентификатор сервера лицензирования удаленный рабочий стол, полученный по телефону или через Интернет.</span><span class="sxs-lookup"><span data-stu-id="f3d95-111">Remote Desktop license server ID that was obtained over the phone or the Internet.</span></span>

</dd> <dt>

<span data-ttu-id="f3d95-112">*ActivationStatus* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f3d95-112">*ActivationStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f3d95-113">Возвращенное состояние активации может иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="f3d95-113">The activation status returned can be one of the following values.</span></span>

<dt>

<span data-ttu-id="f3d95-114">0</span><span class="sxs-lookup"><span data-stu-id="f3d95-114">0</span></span>
</dt> <dd>

<span data-ttu-id="f3d95-115">Сервер лицензий удаленный рабочий стол активирован.</span><span class="sxs-lookup"><span data-stu-id="f3d95-115">The Remote Desktop license server is activated.</span></span>

</dd> <dt>

<span data-ttu-id="f3d95-116">1</span><span class="sxs-lookup"><span data-stu-id="f3d95-116">1</span></span>
</dt> <dd>

<span data-ttu-id="f3d95-117">Сервер лицензирования удаленный рабочий стол не активирован.</span><span class="sxs-lookup"><span data-stu-id="f3d95-117">The Remote Desktop license server is not activated.</span></span>

</dd> <dt>

<span data-ttu-id="f3d95-118">2</span><span class="sxs-lookup"><span data-stu-id="f3d95-118">2</span></span>
</dt> <dd>

<span data-ttu-id="f3d95-119">Произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="f3d95-119">An unknown error occurred.</span></span> <span data-ttu-id="f3d95-120">Неизвестно, активирован ли сервер лицензий удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="f3d95-120">It is not known whether the Remote Desktop license server is activated.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3d95-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f3d95-121">Return value</span></span>

<span data-ttu-id="f3d95-122">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="f3d95-122">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="f3d95-123">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="f3d95-123">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="f3d95-124">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="f3d95-124">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f3d95-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f3d95-125">Remarks</span></span>

<span data-ttu-id="f3d95-126">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="f3d95-126">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="f3d95-127">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="f3d95-127">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f3d95-128">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="f3d95-128">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f3d95-129">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="f3d95-129">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f3d95-130">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="f3d95-130">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f3d95-131">Требования</span><span class="sxs-lookup"><span data-stu-id="f3d95-131">Requirements</span></span>



| <span data-ttu-id="f3d95-132">Требование</span><span class="sxs-lookup"><span data-stu-id="f3d95-132">Requirement</span></span> | <span data-ttu-id="f3d95-133">Значение</span><span class="sxs-lookup"><span data-stu-id="f3d95-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3d95-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f3d95-134">Minimum supported client</span></span><br/> | <span data-ttu-id="f3d95-135">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f3d95-135">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="f3d95-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f3d95-136">Minimum supported server</span></span><br/> | <span data-ttu-id="f3d95-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f3d95-137">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="f3d95-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f3d95-138">Namespace</span></span><br/>                | <span data-ttu-id="f3d95-139">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="f3d95-139">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="f3d95-140">MOF</span><span class="sxs-lookup"><span data-stu-id="f3d95-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f3d95-141"><dt>Тлсвмипров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f3d95-141"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f3d95-142">DLL</span><span class="sxs-lookup"><span data-stu-id="f3d95-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3d95-143"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3d95-143"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3d95-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f3d95-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3d95-145">**\_Тслиценсесервер Win32**</span><span class="sxs-lookup"><span data-stu-id="f3d95-145">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

