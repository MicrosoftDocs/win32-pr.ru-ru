---
title: Метод Активатесервер класса Win32_TSLicenseServer
description: Активация удаленный рабочий стол сервера лицензирования с помощью удаленный рабочий стол идентификатора сервера лицензирования, полученного по телефону или через Интернет.
ms.assetid: 628e87f0-600e-404d-a0b4-35f1570b4fc0
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Активатесервер
- Службы удаленных рабочих столов метода Активатесервер, класс Win32_TSLicenseServer
- Класс Win32_TSLicenseServer службы удаленных рабочих столов, метод Активатесервер
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.ActivateServer
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19db0df0ca9b0bf41fe692ba07fe605dc1e8d5c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682090"
---
# <a name="activateserver-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="abed9-106">Метод Активатесервер \_ класса Win32 тслиценсесервер</span><span class="sxs-lookup"><span data-stu-id="abed9-106">ActivateServer method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="abed9-107">Активация удаленный рабочий стол сервера лицензирования с помощью удаленный рабочий стол идентификатора сервера лицензирования, полученного по телефону или через Интернет.</span><span class="sxs-lookup"><span data-stu-id="abed9-107">Activates the Remote Desktop license server by using a Remote Desktop license server identifier that is obtained over the phone or the Internet.</span></span>

## <a name="syntax"></a><span data-ttu-id="abed9-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="abed9-108">Syntax</span></span>


```mof
uint32 ActivateServer(
  [in]  string sLicenseServerId,
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a><span data-ttu-id="abed9-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="abed9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abed9-110">*слиценсесерверид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="abed9-110">*sLicenseServerId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abed9-111">Идентификатор сервера лицензирования удаленный рабочий стол, полученный по телефону или через Интернет.</span><span class="sxs-lookup"><span data-stu-id="abed9-111">Remote Desktop license server ID that was obtained over the phone or the Internet.</span></span> <span data-ttu-id="abed9-112">Параметр *слиценсесерверид* представляет собой буквенно-цифровую строку длиной 35 символов, которая не может содержать дефисы.</span><span class="sxs-lookup"><span data-stu-id="abed9-112">The *sLicenseServerId* parameter is a 35-character alphanumeric string that cannot include hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="abed9-113">*ActivationStatus* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="abed9-113">*ActivationStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="abed9-114">Возвращенное состояние активации может быть одним из следующих.</span><span class="sxs-lookup"><span data-stu-id="abed9-114">The activation status returned can be one of the following.</span></span>

<dt>

<span data-ttu-id="abed9-115">0</span><span class="sxs-lookup"><span data-stu-id="abed9-115">0</span></span>
</dt> <dd>

<span data-ttu-id="abed9-116">Сервер лицензий удаленный рабочий стол активирован.</span><span class="sxs-lookup"><span data-stu-id="abed9-116">The Remote Desktop license server is activated.</span></span>

</dd> <dt>

<span data-ttu-id="abed9-117">1</span><span class="sxs-lookup"><span data-stu-id="abed9-117">1</span></span>
</dt> <dd>

<span data-ttu-id="abed9-118">Сервер лицензирования удаленный рабочий стол не активирован.</span><span class="sxs-lookup"><span data-stu-id="abed9-118">The Remote Desktop license server is not activated.</span></span>

</dd> <dt>

<span data-ttu-id="abed9-119">2</span><span class="sxs-lookup"><span data-stu-id="abed9-119">2</span></span>
</dt> <dd>

<span data-ttu-id="abed9-120">Произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="abed9-120">An unknown error occurred.</span></span> <span data-ttu-id="abed9-121">Неизвестно, активирован ли сервер лицензий удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="abed9-121">It is not known whether the Remote Desktop license server is activated.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abed9-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="abed9-122">Return value</span></span>

<span data-ttu-id="abed9-123">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="abed9-123">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="abed9-124">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="abed9-124">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="abed9-125">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="abed9-125">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="abed9-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="abed9-126">Remarks</span></span>

<span data-ttu-id="abed9-127">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="abed9-127">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="abed9-128">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="abed9-128">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="abed9-129">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="abed9-129">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="abed9-130">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="abed9-130">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="abed9-131">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="abed9-131">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="abed9-132">Требования</span><span class="sxs-lookup"><span data-stu-id="abed9-132">Requirements</span></span>



| <span data-ttu-id="abed9-133">Требование</span><span class="sxs-lookup"><span data-stu-id="abed9-133">Requirement</span></span> | <span data-ttu-id="abed9-134">Значение</span><span class="sxs-lookup"><span data-stu-id="abed9-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="abed9-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="abed9-135">Minimum supported client</span></span><br/> | <span data-ttu-id="abed9-136">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="abed9-136">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="abed9-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="abed9-137">Minimum supported server</span></span><br/> | <span data-ttu-id="abed9-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="abed9-138">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="abed9-139">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="abed9-139">Namespace</span></span><br/>                | <span data-ttu-id="abed9-140">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="abed9-140">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="abed9-141">MOF</span><span class="sxs-lookup"><span data-stu-id="abed9-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="abed9-142"><dt>Тлсвмипров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="abed9-142"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="abed9-143">DLL</span><span class="sxs-lookup"><span data-stu-id="abed9-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="abed9-144"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="abed9-144"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abed9-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="abed9-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abed9-146">**\_Тслиценсесервер Win32**</span><span class="sxs-lookup"><span data-stu-id="abed9-146">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

