---
title: Метод FileExtensions класса Win32_TSApplicationFileExtensions
description: Предоставляет список расширений имен файлов, обрабатываемых приложением.
ms.assetid: 833a1b68-86ed-4361-bbcb-a8d1c4a9306d
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода FileExtensions
- Службы удаленных рабочих столов метода FileExtensions, класс Win32_TSApplicationFileExtensions
- Класс Win32_TSApplicationFileExtensions службы удаленных рабочих столов, метод FileExtensions
topic_type:
- apiref
api_name:
- Win32_TSApplicationFileExtensions.FileExtensions
api_location:
- TsPubWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5aa0bff92cdc274c8dba56aa11a44791e3ad9f01
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989253"
---
# <a name="fileextensions-method-of-the-win32_tsapplicationfileextensions-class"></a><span data-ttu-id="7514e-106">Метод FileExtensions \_ класса Win32 тсаппликатионфиликстенсионс</span><span class="sxs-lookup"><span data-stu-id="7514e-106">FileExtensions method of the Win32\_TSApplicationFileExtensions class</span></span>

<span data-ttu-id="7514e-107">Предоставляет список расширений имен файлов, обрабатываемых приложением.</span><span class="sxs-lookup"><span data-stu-id="7514e-107">Provides a list of the file name extensions that are handled by an application.</span></span>

## <a name="syntax"></a><span data-ttu-id="7514e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7514e-108">Syntax</span></span>


```mof
uint32 FileExtensions(
  [in]  string AppPath,
  [out] string Extensions[]
);
```



## <a name="parameters"></a><span data-ttu-id="7514e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="7514e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7514e-110">*Апппас* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7514e-110">*AppPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7514e-111">Путь к приложению.</span><span class="sxs-lookup"><span data-stu-id="7514e-111">The path of the application.</span></span>

</dd> <dt>

<span data-ttu-id="7514e-112">*Расширения* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7514e-112">*Extensions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7514e-113">Расширения имен файлов, обрабатываемые приложением.</span><span class="sxs-lookup"><span data-stu-id="7514e-113">The file name extensions that are handled by the application.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7514e-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7514e-114">Remarks</span></span>

<span data-ttu-id="7514e-115">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="7514e-115">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="7514e-116">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="7514e-116">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="7514e-117">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="7514e-117">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="7514e-118">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="7514e-118">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="7514e-119">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="7514e-119">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="7514e-120">Требования</span><span class="sxs-lookup"><span data-stu-id="7514e-120">Requirements</span></span>



| <span data-ttu-id="7514e-121">Требование</span><span class="sxs-lookup"><span data-stu-id="7514e-121">Requirement</span></span> | <span data-ttu-id="7514e-122">Значение</span><span class="sxs-lookup"><span data-stu-id="7514e-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7514e-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7514e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="7514e-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="7514e-124">None supported</span></span><br/>                                                               |
| <span data-ttu-id="7514e-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7514e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="7514e-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7514e-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7514e-127">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7514e-127">Namespace</span></span><br/>                | <span data-ttu-id="7514e-128">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="7514e-128">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="7514e-129">MOF</span><span class="sxs-lookup"><span data-stu-id="7514e-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7514e-130"><dt>Тсаллов. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7514e-130"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="7514e-131">DLL</span><span class="sxs-lookup"><span data-stu-id="7514e-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7514e-132"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7514e-132"><dt>TsPubWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7514e-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7514e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7514e-134">**\_Тсаппликатионфиликстенсионс Win32**</span><span class="sxs-lookup"><span data-stu-id="7514e-134">**Win32\_TSApplicationFileExtensions**</span></span>](win32-tsapplicationfileextensions.md)
</dt> </dl>

 

