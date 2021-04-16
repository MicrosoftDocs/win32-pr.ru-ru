---
title: Метод Иссекуреакцессалловед класса Win32_TSLicenseServer
description: Получает значение, указывающее, разрешен ли серверу узла сеансов удаленный рабочий стол (узлу сеансов удаленных рабочих столов) запрос службы удаленных рабочих столов лицензий клиентского доступа (RDS \ 160; CAL) с сервера лицензий удаленный рабочий стол.
ms.assetid: b9124808-79be-4b94-b12b-f093d5e8195a
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Иссекуреакцессалловед
- Службы удаленных рабочих столов метода Иссекуреакцессалловед, класс Win32_TSLicenseServer
- Класс Win32_TSLicenseServer службы удаленных рабочих столов, метод Иссекуреакцессалловед
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsSecureAccessAllowed
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf35fd8b38139027955fde51a209000435744f5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534127"
---
# <a name="issecureaccessallowed-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="90156-106">Метод Иссекуреакцессалловед \_ класса Win32 тслиценсесервер</span><span class="sxs-lookup"><span data-stu-id="90156-106">IsSecureAccessAllowed method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="90156-107">Получает значение, указывающее, разрешено ли серверу удаленный рабочий стол узла сеансов (удаленным рабочим стол) запрос службы удаленных рабочих столов клиентских лицензий (RDS CAL) с сервера лицензий удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="90156-107">Retrieves whether a Remote Desktop Session Host (RD Session Host) server is allowed to request Remote Desktop Services client access licenses (RDS CALs) from the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="90156-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="90156-108">Syntax</span></span>


```mof
uint32 IsSecureAccessAllowed(
  [in]  string  tsname,
  [out] boolean Allowed
);
```



## <a name="parameters"></a><span data-ttu-id="90156-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="90156-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90156-110">*тснаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="90156-110">*tsname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90156-111">Имя сервера узла сеансов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="90156-111">Name of the RD Session Host server.</span></span>

</dd> <dt>

<span data-ttu-id="90156-112">*Разрешено* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="90156-112">*Allowed* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="90156-113">Логическое значение, указывающее, разрешено ли серверу узла сеансов удаленных рабочих столов запрашивать клиентские лицензии RDS с сервера лицензирования.</span><span class="sxs-lookup"><span data-stu-id="90156-113">Boolean value that indicates whether the RD Session Host server is allowed to request RDS CALs from the license server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90156-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="90156-114">Return value</span></span>

<span data-ttu-id="90156-115">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="90156-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="90156-116">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="90156-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="90156-117">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="90156-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="90156-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="90156-118">Remarks</span></span>

<span data-ttu-id="90156-119">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="90156-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="90156-120">Возвращаемое значение основано на параметре групповой политики "Группа безопасности сервера лицензий" и членстве в локальной группе "компьютеры сервера терминалов" на сервере лицензирования удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="90156-120">The returned value is based on the "license server security group" group policy setting, and membership in the Terminal Server Computers local group on the Remote Desktop license server.</span></span>

<span data-ttu-id="90156-121">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="90156-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="90156-122">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="90156-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="90156-123">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="90156-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="90156-124">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="90156-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="90156-125">Требования</span><span class="sxs-lookup"><span data-stu-id="90156-125">Requirements</span></span>



| <span data-ttu-id="90156-126">Требование</span><span class="sxs-lookup"><span data-stu-id="90156-126">Requirement</span></span> | <span data-ttu-id="90156-127">Значение</span><span class="sxs-lookup"><span data-stu-id="90156-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="90156-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="90156-128">Minimum supported client</span></span><br/> | <span data-ttu-id="90156-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="90156-129">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="90156-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="90156-130">Minimum supported server</span></span><br/> | <span data-ttu-id="90156-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="90156-131">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="90156-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="90156-132">Namespace</span></span><br/>                | <span data-ttu-id="90156-133">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="90156-133">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="90156-134">MOF</span><span class="sxs-lookup"><span data-stu-id="90156-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="90156-135"><dt>Тлсвмипров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="90156-135"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="90156-136">DLL</span><span class="sxs-lookup"><span data-stu-id="90156-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90156-137"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="90156-137"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90156-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="90156-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90156-139">**\_Тслиценсесервер Win32**</span><span class="sxs-lookup"><span data-stu-id="90156-139">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> <dt>

[<span data-ttu-id="90156-140">**ислссекгрпгпенаблед**</span><span class="sxs-lookup"><span data-stu-id="90156-140">**IsLSSecGrpGPEnabled**</span></span>](islssecgrpgpenabled-win32-tslicenseserver.md)
</dt> </dl>

 

