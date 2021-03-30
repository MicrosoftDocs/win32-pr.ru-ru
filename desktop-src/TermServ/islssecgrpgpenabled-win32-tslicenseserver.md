---
title: Метод Ислссекгрпгпенаблед класса Win32_TSLicenseServer
description: Получает значение, указывающее, является ли группа безопасности \ 0034; сервера лицензирования \ 0034; параметр групповой политики включен на сервере лицензирования удаленный рабочий стол.
ms.assetid: 715b619b-f082-4fed-ac4c-70d5e286e37c
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Ислссекгрпгпенаблед
- Службы удаленных рабочих столов метода Ислссекгрпгпенаблед, класс Win32_TSLicenseServer
- Класс Win32_TSLicenseServer службы удаленных рабочих столов, метод Ислссекгрпгпенаблед
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSSecGrpGPEnabled
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27f3d7ec9de3d98849f9680f1b2a87bf5b22922a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136314"
---
# <a name="islssecgrpgpenabled-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="d8c78-106">Метод Ислссекгрпгпенаблед \_ класса Win32 тслиценсесервер</span><span class="sxs-lookup"><span data-stu-id="d8c78-106">IsLSSecGrpGPEnabled method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="d8c78-107">Возвращает значение, указывающее, включен ли параметр групповой политики "Группа безопасности сервера лицензирования" на сервере лицензирования удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="d8c78-107">Retrieves whether the "license server security group" group policy setting is enabled on the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8c78-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d8c78-108">Syntax</span></span>


```mof
uint32 IsLSSecGrpGPEnabled(
  [out] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="d8c78-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d8c78-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8c78-110">*Включено* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d8c78-110">*Enabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d8c78-111">Логическое значение, указывающее, включен ли параметр политики "Группа безопасности сервера лицензий".</span><span class="sxs-lookup"><span data-stu-id="d8c78-111">Boolean value that indicates whether the "license server security group" policy setting is enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8c78-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d8c78-112">Return value</span></span>

<span data-ttu-id="d8c78-113">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="d8c78-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="d8c78-114">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="d8c78-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="d8c78-115">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="d8c78-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d8c78-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d8c78-116">Remarks</span></span>

<span data-ttu-id="d8c78-117">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="d8c78-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="d8c78-118">Параметр политики "Группа безопасности сервера лицензий" позволяет указать серверы узла сеансов удаленный рабочий стол (узлы сеансов удаленных рабочих столов), которым разрешено подключение к серверу лицензирования для получения службы удаленных рабочих столов клиентских лицензий (RDS CAL).</span><span class="sxs-lookup"><span data-stu-id="d8c78-118">The "license server security group" policy setting allows you to specify the Remote Desktop Session Host (RD Session Host) servers that are permitted to contact the license server to obtain Remote Desktop Services client access licenses (RDS CALs).</span></span> <span data-ttu-id="d8c78-119">Если на сервере лицензирования включен параметр политики, то сервер будет отвечать только на запросы клиентских лицензий служб удаленных рабочих столов, которые являются членами локальной группы "компьютеры сервера терминалов" на сервере лицензирования.</span><span class="sxs-lookup"><span data-stu-id="d8c78-119">If the policy setting is enabled on the license server, the server will only respond to RDS CAL requests from RD Session Host servers whose computer accounts are members of the Terminal Server Computers local group on the license server.</span></span>

<span data-ttu-id="d8c78-120">Параметр политики находится в следующем узле редактора локальных групповых политик:</span><span class="sxs-lookup"><span data-stu-id="d8c78-120">The policy setting is located in the following node of the local group policy editor:</span></span>

<span data-ttu-id="d8c78-121">Конфигурация компьютера \\ Административные шаблоны \\ компоненты Windows \\ \\ Лицензирование служб терминалов</span><span class="sxs-lookup"><span data-stu-id="d8c78-121">Computer Configuration\\Administrative Templates\\Windows Components\\Terminal Services\\TS Licensing</span></span>

<span data-ttu-id="d8c78-122">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="d8c78-122">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d8c78-123">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="d8c78-123">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="d8c78-124">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="d8c78-124">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d8c78-125">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="d8c78-125">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="d8c78-126">Требования</span><span class="sxs-lookup"><span data-stu-id="d8c78-126">Requirements</span></span>



| <span data-ttu-id="d8c78-127">Требование</span><span class="sxs-lookup"><span data-stu-id="d8c78-127">Requirement</span></span> | <span data-ttu-id="d8c78-128">Значение</span><span class="sxs-lookup"><span data-stu-id="d8c78-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8c78-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d8c78-129">Minimum supported client</span></span><br/> | <span data-ttu-id="d8c78-130">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d8c78-130">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="d8c78-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d8c78-131">Minimum supported server</span></span><br/> | <span data-ttu-id="d8c78-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d8c78-132">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="d8c78-133">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d8c78-133">Namespace</span></span><br/>                | <span data-ttu-id="d8c78-134">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="d8c78-134">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="d8c78-135">MOF</span><span class="sxs-lookup"><span data-stu-id="d8c78-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d8c78-136"><dt>Тлсвмипров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d8c78-136"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="d8c78-137">DLL</span><span class="sxs-lookup"><span data-stu-id="d8c78-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8c78-138"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8c78-138"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8c78-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d8c78-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8c78-140">**\_Тслиценсесервер Win32**</span><span class="sxs-lookup"><span data-stu-id="d8c78-140">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

