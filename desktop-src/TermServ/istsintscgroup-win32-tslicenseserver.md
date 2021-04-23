---
title: Метод Истсинтскграуп класса Win32_TSLicenseServer
description: Получает значение, указывающее, входит ли сервер узла сеансов удаленный рабочий стол (узел сеансов удаленных рабочих столов) в локальную группу "компьютеры сервера терминалов" на сервере лицензирования удаленный рабочий стол.
ms.assetid: 61c39928-3a2b-4a36-ae4e-b9597a12d5e7
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Истсинтскграуп
- Службы удаленных рабочих столов метода Истсинтскграуп, класс Win32_TSLicenseServer
- Класс Win32_TSLicenseServer службы удаленных рабочих столов, метод Истсинтскграуп
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsTSinTSCGroup
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d666457f053c8fd48abd904d099bfbfa93a0de6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535216"
---
# <a name="istsintscgroup-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="989fb-106">Метод Истсинтскграуп \_ класса Win32 тслиценсесервер</span><span class="sxs-lookup"><span data-stu-id="989fb-106">IsTSinTSCGroup method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="989fb-107">Получает значение, указывающее, входит ли сервер узла сеансов удаленный рабочий стол (узел сеансов удаленных рабочих столов) в локальную группу "компьютеры сервера терминалов" на сервере лицензирования удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="989fb-107">Retrieves whether a Remote Desktop Session Host (RD Session Host) server is a member of the Terminal Server Computers local group on the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="989fb-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="989fb-108">Syntax</span></span>


```mof
uint32 IsTSinTSCGroup(
  [in]  string  tsname,
  [out] boolean IsMember
);
```



## <a name="parameters"></a><span data-ttu-id="989fb-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="989fb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="989fb-110">*тснаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="989fb-110">*tsname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="989fb-111">Имя сервера узла сеансов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="989fb-111">Name of the RD Session Host server.</span></span>

</dd> <dt>

<span data-ttu-id="989fb-112">*Элемент* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="989fb-112">*IsMember* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="989fb-113">Логическое значение, указывающее, является ли сервер узла сеансов удаленных рабочих столов членом локальной группы "компьютеры сервера терминалов".</span><span class="sxs-lookup"><span data-stu-id="989fb-113">Boolean value that indicates whether the RD Session Host server is a member of the Terminal Server Computers local group.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="989fb-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="989fb-114">Return value</span></span>

<span data-ttu-id="989fb-115">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="989fb-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="989fb-116">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="989fb-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="989fb-117">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="989fb-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="989fb-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="989fb-118">Remarks</span></span>

<span data-ttu-id="989fb-119">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="989fb-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="989fb-120">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="989fb-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="989fb-121">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="989fb-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="989fb-122">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="989fb-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="989fb-123">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="989fb-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="989fb-124">Требования</span><span class="sxs-lookup"><span data-stu-id="989fb-124">Requirements</span></span>



| <span data-ttu-id="989fb-125">Требование</span><span class="sxs-lookup"><span data-stu-id="989fb-125">Requirement</span></span> | <span data-ttu-id="989fb-126">Значение</span><span class="sxs-lookup"><span data-stu-id="989fb-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="989fb-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="989fb-127">Minimum supported client</span></span><br/> | <span data-ttu-id="989fb-128">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="989fb-128">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="989fb-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="989fb-129">Minimum supported server</span></span><br/> | <span data-ttu-id="989fb-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="989fb-130">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="989fb-131">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="989fb-131">Namespace</span></span><br/>                | <span data-ttu-id="989fb-132">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="989fb-132">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="989fb-133">MOF</span><span class="sxs-lookup"><span data-stu-id="989fb-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="989fb-134"><dt>Тлсвмипров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="989fb-134"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="989fb-135">DLL</span><span class="sxs-lookup"><span data-stu-id="989fb-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="989fb-136"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="989fb-136"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="989fb-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="989fb-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="989fb-138">**\_Тслиценсесервер Win32**</span><span class="sxs-lookup"><span data-stu-id="989fb-138">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

