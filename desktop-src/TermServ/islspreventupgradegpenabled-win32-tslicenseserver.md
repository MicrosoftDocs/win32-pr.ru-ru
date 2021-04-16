---
title: Метод Ислспревентупградегпенаблед класса Win32_TSLicenseServer
description: Получает значение, определяющее, будет ли параметр \ 0034; предотвращать обновление лицензии \ 0034; параметр групповой политики включен на сервере лицензирования удаленный рабочий стол.
ms.assetid: f78585b8-a50c-402b-ab20-f405eba0c079
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Ислспревентупградегпенаблед
- Службы удаленных рабочих столов метода Ислспревентупградегпенаблед, класс Win32_TSLicenseServer
- Класс Win32_TSLicenseServer службы удаленных рабочих столов, метод Ислспревентупградегпенаблед
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSPreventUpgradeGPEnabled
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 205dc1ac05f5dca44297f8d80653ad51b7518d38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672720"
---
# <a name="islspreventupgradegpenabled-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="8a7cd-106">Метод Ислспревентупградегпенаблед \_ класса Win32 тслиценсесервер</span><span class="sxs-lookup"><span data-stu-id="8a7cd-106">IsLSPreventUpgradeGPEnabled method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="8a7cd-107">Получает значение, указывающее, включен ли параметр групповой политики "запретить обновление лицензий" на сервере лицензирования удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="8a7cd-107">Retrieves whether the "prevent license upgrade" group policy setting is enabled on the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a7cd-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8a7cd-108">Syntax</span></span>


```mof
uint32 IsLSPreventUpgradeGPEnabled(
  [out] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="8a7cd-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="8a7cd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a7cd-110">*Включено* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8a7cd-110">*Enabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a7cd-111">Логическое значение, указывающее, включен ли параметр политики "запретить обновление лицензий".</span><span class="sxs-lookup"><span data-stu-id="8a7cd-111">Boolean value that indicates whether the "prevent license upgrade" policy setting is enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a7cd-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8a7cd-112">Return value</span></span>

<span data-ttu-id="8a7cd-113">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="8a7cd-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="8a7cd-114">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="8a7cd-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="8a7cd-115">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="8a7cd-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8a7cd-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8a7cd-116">Remarks</span></span>

<span data-ttu-id="8a7cd-117">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="8a7cd-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="8a7cd-118">Если параметр политики "запретить обновление лицензий" включен, сервер лицензирования выдаст клиенту только временную клиентскую лицензию RDS, если соответствующая клиентская лицензия RDS для сервера узла сеансов удаленный рабочий стол (узел сеансов удаленных рабочих столов) недоступна.</span><span class="sxs-lookup"><span data-stu-id="8a7cd-118">If the "prevent license upgrade" policy setting is enabled, the license server will only issue a temporary RDS CAL to the client if an appropriate RDS CAL for the Remote Desktop Session Host (RD Session Host) server is not available.</span></span>

<span data-ttu-id="8a7cd-119">Параметр политики находится в следующем узле редактора локальных групповых политик:</span><span class="sxs-lookup"><span data-stu-id="8a7cd-119">The policy setting is located in the following node of the local group policy editor:</span></span>

<span data-ttu-id="8a7cd-120">Конфигурация компьютера \\ Административные шаблоны \\ компоненты Windows \\ \\ Лицензирование служб терминалов</span><span class="sxs-lookup"><span data-stu-id="8a7cd-120">Computer Configuration\\Administrative Templates\\Windows Components\\Terminal Services\\TS Licensing</span></span>

<span data-ttu-id="8a7cd-121">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="8a7cd-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="8a7cd-122">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="8a7cd-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="8a7cd-123">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="8a7cd-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="8a7cd-124">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="8a7cd-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="8a7cd-125">Требования</span><span class="sxs-lookup"><span data-stu-id="8a7cd-125">Requirements</span></span>



| <span data-ttu-id="8a7cd-126">Требование</span><span class="sxs-lookup"><span data-stu-id="8a7cd-126">Requirement</span></span> | <span data-ttu-id="8a7cd-127">Значение</span><span class="sxs-lookup"><span data-stu-id="8a7cd-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a7cd-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8a7cd-128">Minimum supported client</span></span><br/> | <span data-ttu-id="8a7cd-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8a7cd-129">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="8a7cd-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8a7cd-130">Minimum supported server</span></span><br/> | <span data-ttu-id="8a7cd-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8a7cd-131">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="8a7cd-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8a7cd-132">Namespace</span></span><br/>                | <span data-ttu-id="8a7cd-133">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="8a7cd-133">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="8a7cd-134">MOF</span><span class="sxs-lookup"><span data-stu-id="8a7cd-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8a7cd-135"><dt>Тлсвмипров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8a7cd-135"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="8a7cd-136">DLL</span><span class="sxs-lookup"><span data-stu-id="8a7cd-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a7cd-137"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a7cd-137"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a7cd-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8a7cd-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a7cd-139">**\_Тслиценсесервер Win32**</span><span class="sxs-lookup"><span data-stu-id="8a7cd-139">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

