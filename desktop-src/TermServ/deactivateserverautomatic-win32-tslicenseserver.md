---
title: Метод Деактиватесервераутоматик класса Win32_TSLicenseServer
description: Деактивирует сервер лицензий удаленный рабочий стол через Интернет.
ms.assetid: 6e049d7f-1753-484d-98b8-fde66d16b5ab
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Деактиватесервераутоматик
- Службы удаленных рабочих столов метода Деактиватесервераутоматик, класс Win32_TSLicenseServer
- Класс Win32_TSLicenseServer службы удаленных рабочих столов, метод Деактиватесервераутоматик
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.DeactivateServerAutomatic
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d466b5f7814d6004bafdd01bce161a481eacf26a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071286"
---
# <a name="deactivateserverautomatic-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="5962d-106">Метод Деактиватесервераутоматик \_ класса Win32 тслиценсесервер</span><span class="sxs-lookup"><span data-stu-id="5962d-106">DeactivateServerAutomatic method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="5962d-107">Деактивирует сервер лицензий удаленный рабочий стол через Интернет.</span><span class="sxs-lookup"><span data-stu-id="5962d-107">Deactivates the Remote Desktop license server over the Internet.</span></span>

## <a name="syntax"></a><span data-ttu-id="5962d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5962d-108">Syntax</span></span>


```mof
uint32 DeactivateServerAutomatic(
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a><span data-ttu-id="5962d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="5962d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5962d-110">*ActivationStatus* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5962d-110">*ActivationStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5962d-111">Возвращенное состояние активации может быть одним из следующих.</span><span class="sxs-lookup"><span data-stu-id="5962d-111">The activation status returned can be one of the following.</span></span>

<dt>

<span data-ttu-id="5962d-112">0</span><span class="sxs-lookup"><span data-stu-id="5962d-112">0</span></span>
</dt> <dd>

<span data-ttu-id="5962d-113">Сервер лицензий удаленный рабочий стол активирован.</span><span class="sxs-lookup"><span data-stu-id="5962d-113">The Remote Desktop license server is activated.</span></span>

</dd> <dt>

<span data-ttu-id="5962d-114">1</span><span class="sxs-lookup"><span data-stu-id="5962d-114">1</span></span>
</dt> <dd>

<span data-ttu-id="5962d-115">Сервер лицензирования удаленный рабочий стол не активирован.</span><span class="sxs-lookup"><span data-stu-id="5962d-115">The Remote Desktop license server is not activated.</span></span>

</dd> <dt>

<span data-ttu-id="5962d-116">2</span><span class="sxs-lookup"><span data-stu-id="5962d-116">2</span></span>
</dt> <dd>

<span data-ttu-id="5962d-117">Произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="5962d-117">An unknown error occurred.</span></span> <span data-ttu-id="5962d-118">Неизвестно, активирован ли сервер лицензий удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="5962d-118">It is not known whether the Remote Desktop license server is activated.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5962d-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5962d-119">Return value</span></span>

<span data-ttu-id="5962d-120">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="5962d-120">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="5962d-121">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="5962d-121">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="5962d-122">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="5962d-122">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5962d-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5962d-123">Remarks</span></span>

<span data-ttu-id="5962d-124">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="5962d-124">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="5962d-125">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="5962d-125">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5962d-126">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="5962d-126">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="5962d-127">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="5962d-127">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5962d-128">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="5962d-128">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="5962d-129">Требования</span><span class="sxs-lookup"><span data-stu-id="5962d-129">Requirements</span></span>



| <span data-ttu-id="5962d-130">Требование</span><span class="sxs-lookup"><span data-stu-id="5962d-130">Requirement</span></span> | <span data-ttu-id="5962d-131">Значение</span><span class="sxs-lookup"><span data-stu-id="5962d-131">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="5962d-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5962d-132">Minimum supported client</span></span><br/> | <span data-ttu-id="5962d-133">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="5962d-133">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="5962d-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5962d-134">Minimum supported server</span></span><br/> | <span data-ttu-id="5962d-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5962d-135">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="5962d-136">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="5962d-136">Namespace</span></span><br/>                | <span data-ttu-id="5962d-137">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="5962d-137">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="5962d-138">MOF</span><span class="sxs-lookup"><span data-stu-id="5962d-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5962d-139"><dt>Тлсвмипров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5962d-139"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="5962d-140">DLL</span><span class="sxs-lookup"><span data-stu-id="5962d-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5962d-141"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5962d-141"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5962d-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5962d-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5962d-143">**\_Тслиценсесервер Win32**</span><span class="sxs-lookup"><span data-stu-id="5962d-143">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

