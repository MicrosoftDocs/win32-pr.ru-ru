---
title: Метод Реактиватесервераутоматик класса Win32_TSLicenseServer
description: Повторно активирует сервер лицензий удаленный рабочий стол, используя автоматическое подключение к Интернету.
ms.assetid: 98b9b8e5-4de4-418c-9175-58e8b84784d5
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Реактиватесервераутоматик
- Службы удаленных рабочих столов метода Реактиватесервераутоматик, класс Win32_TSLicenseServer
- Класс Win32_TSLicenseServer службы удаленных рабочих столов, метод Реактиватесервераутоматик
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.ReactivateServerAutomatic
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81b9df7314abc3dccf6458322911c50d6120ad10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682072"
---
# <a name="reactivateserverautomatic-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="733bc-106">Метод Реактиватесервераутоматик \_ класса Win32 тслиценсесервер</span><span class="sxs-lookup"><span data-stu-id="733bc-106">ReactivateServerAutomatic method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="733bc-107">Повторно активирует сервер лицензий удаленный рабочий стол, используя автоматическое подключение к Интернету.</span><span class="sxs-lookup"><span data-stu-id="733bc-107">Reactivates the Remote Desktop license server by using an automatic connection to the Internet.</span></span>

## <a name="syntax"></a><span data-ttu-id="733bc-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="733bc-108">Syntax</span></span>


```mof
uint32 ReactivateServerAutomatic(
  [in]  uint32 Reason,
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a><span data-ttu-id="733bc-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="733bc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="733bc-110">*Причина* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="733bc-110">*Reason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="733bc-111">Причина активации.</span><span class="sxs-lookup"><span data-stu-id="733bc-111">Reason for the activation.</span></span> <span data-ttu-id="733bc-112">Может быть одним из указанных далее.</span><span class="sxs-lookup"><span data-stu-id="733bc-112">It can be one of the following values.</span></span>

<dt>

<span data-ttu-id="733bc-113">0</span><span class="sxs-lookup"><span data-stu-id="733bc-113">0</span></span>
</dt> <dd>

<span data-ttu-id="733bc-114">Сервер был повторно развернут.</span><span class="sxs-lookup"><span data-stu-id="733bc-114">The server was redeployed.</span></span>

</dd> <dt>

<span data-ttu-id="733bc-115">1</span><span class="sxs-lookup"><span data-stu-id="733bc-115">1</span></span>
</dt> <dd>

<span data-ttu-id="733bc-116">Сертификат поврежден.</span><span class="sxs-lookup"><span data-stu-id="733bc-116">The certificate was corrupt.</span></span>

</dd> <dt>

<span data-ttu-id="733bc-117">2</span><span class="sxs-lookup"><span data-stu-id="733bc-117">2</span></span>
</dt> <dd>

<span data-ttu-id="733bc-118">Закрытый ключ скомпрометирован.</span><span class="sxs-lookup"><span data-stu-id="733bc-118">The private key was compromised.</span></span>

</dd> <dt>

<span data-ttu-id="733bc-119">3</span><span class="sxs-lookup"><span data-stu-id="733bc-119">3</span></span>
</dt> <dd>

<span data-ttu-id="733bc-120">Срок действия ключа активации истек.</span><span class="sxs-lookup"><span data-stu-id="733bc-120">The activation key expired.</span></span>

</dd> <dt>

<span data-ttu-id="733bc-121">4</span><span class="sxs-lookup"><span data-stu-id="733bc-121">4</span></span>
</dt> <dd>

<span data-ttu-id="733bc-122">Сервер был обновлен.</span><span class="sxs-lookup"><span data-stu-id="733bc-122">The server was upgraded.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="733bc-123">*ActivationStatus* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="733bc-123">*ActivationStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="733bc-124">Возвращенное состояние активации может иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="733bc-124">The activation status returned can be one of the following values.</span></span>

<dt>

<span data-ttu-id="733bc-125">0</span><span class="sxs-lookup"><span data-stu-id="733bc-125">0</span></span>
</dt> <dd>

<span data-ttu-id="733bc-126">Сервер лицензий удаленный рабочий стол активирован.</span><span class="sxs-lookup"><span data-stu-id="733bc-126">The Remote Desktop license server is activated.</span></span>

</dd> <dt>

<span data-ttu-id="733bc-127">1</span><span class="sxs-lookup"><span data-stu-id="733bc-127">1</span></span>
</dt> <dd>

<span data-ttu-id="733bc-128">Сервер лицензирования удаленный рабочий стол не активирован.</span><span class="sxs-lookup"><span data-stu-id="733bc-128">The Remote Desktop license server is not activated.</span></span>

</dd> <dt>

<span data-ttu-id="733bc-129">2</span><span class="sxs-lookup"><span data-stu-id="733bc-129">2</span></span>
</dt> <dd>

<span data-ttu-id="733bc-130">Произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="733bc-130">An unknown error occurred.</span></span> <span data-ttu-id="733bc-131">Неизвестно, активирован ли сервер лицензий удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="733bc-131">It is not known whether the Remote Desktop license server is activated.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="733bc-132">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="733bc-132">Return value</span></span>

<span data-ttu-id="733bc-133">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="733bc-133">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="733bc-134">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="733bc-134">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="733bc-135">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="733bc-135">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="733bc-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="733bc-136">Remarks</span></span>

<span data-ttu-id="733bc-137">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="733bc-137">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="733bc-138">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="733bc-138">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="733bc-139">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="733bc-139">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="733bc-140">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="733bc-140">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="733bc-141">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="733bc-141">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="733bc-142">Требования</span><span class="sxs-lookup"><span data-stu-id="733bc-142">Requirements</span></span>



| <span data-ttu-id="733bc-143">Требование</span><span class="sxs-lookup"><span data-stu-id="733bc-143">Requirement</span></span> | <span data-ttu-id="733bc-144">Значение</span><span class="sxs-lookup"><span data-stu-id="733bc-144">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="733bc-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="733bc-145">Minimum supported client</span></span><br/> | <span data-ttu-id="733bc-146">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="733bc-146">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="733bc-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="733bc-147">Minimum supported server</span></span><br/> | <span data-ttu-id="733bc-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="733bc-148">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="733bc-149">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="733bc-149">Namespace</span></span><br/>                | <span data-ttu-id="733bc-150">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="733bc-150">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="733bc-151">MOF</span><span class="sxs-lookup"><span data-stu-id="733bc-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="733bc-152"><dt>Тлсвмипров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="733bc-152"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="733bc-153">DLL</span><span class="sxs-lookup"><span data-stu-id="733bc-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="733bc-154"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="733bc-154"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="733bc-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="733bc-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="733bc-156">**\_Тслиценсесервер Win32**</span><span class="sxs-lookup"><span data-stu-id="733bc-156">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

