---
title: Метод EnvironmentVariables класса Win32_TSExpandEnvironmentVariables
description: Расширяет переменные среды, определенные системой. | Метод EnvironmentVariables класса Win32_TSExpandEnvironmentVariables
ms.assetid: eff0dcdf-ef98-4730-9b0c-4f44250a607b
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода EnvironmentVariables
- Службы удаленных рабочих столов метода EnvironmentVariables, класс Win32_TSExpandEnvironmentVariables
- Класс Win32_TSExpandEnvironmentVariables службы удаленных рабочих столов, метод EnvironmentVariables
topic_type:
- apiref
api_name:
- Win32_TSExpandEnvironmentVariables.EnvironmentVariables
api_location:
- TsPubWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6f038ee1d5f93c11336657f9b8c1a80ecc05d6d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105674591"
---
# <a name="environmentvariables-method-of-the-win32_tsexpandenvironmentvariables-class"></a><span data-ttu-id="d4d8f-107">Метод EnvironmentVariables \_ класса Win32 тсекспанденвиронментвариаблес</span><span class="sxs-lookup"><span data-stu-id="d4d8f-107">EnvironmentVariables method of the Win32\_TSExpandEnvironmentVariables class</span></span>

<span data-ttu-id="d4d8f-108">Расширяет переменные среды, определенные системой.</span><span class="sxs-lookup"><span data-stu-id="d4d8f-108">Expands system-defined environment variables.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4d8f-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d4d8f-109">Syntax</span></span>


```mof
uint32 EnvironmentVariables(
  [in]  string OriginalString,
  [out] string ExpandedString
);
```



## <a name="parameters"></a><span data-ttu-id="d4d8f-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="d4d8f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4d8f-111">*OriginalString* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d4d8f-111">*OriginalString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4d8f-112">Строка, содержащая переменные среды для расширения.</span><span class="sxs-lookup"><span data-stu-id="d4d8f-112">A string that contains the environment variables to expand.</span></span>

</dd> <dt>

<span data-ttu-id="d4d8f-113">*Експандедстринг* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d4d8f-113">*ExpandedString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d4d8f-114">Строка с развернутыми переменными среды.</span><span class="sxs-lookup"><span data-stu-id="d4d8f-114">A string with the environment variables expanded.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d4d8f-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d4d8f-115">Remarks</span></span>

<span data-ttu-id="d4d8f-116">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="d4d8f-116">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="d4d8f-117">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="d4d8f-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d4d8f-118">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="d4d8f-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="d4d8f-119">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="d4d8f-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d4d8f-120">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="d4d8f-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="d4d8f-121">Требования</span><span class="sxs-lookup"><span data-stu-id="d4d8f-121">Requirements</span></span>



| <span data-ttu-id="d4d8f-122">Требование</span><span class="sxs-lookup"><span data-stu-id="d4d8f-122">Requirement</span></span> | <span data-ttu-id="d4d8f-123">Значение</span><span class="sxs-lookup"><span data-stu-id="d4d8f-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4d8f-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d4d8f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d4d8f-125">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d4d8f-125">None supported</span></span><br/>                                                               |
| <span data-ttu-id="d4d8f-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d4d8f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d4d8f-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d4d8f-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d4d8f-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d4d8f-128">Namespace</span></span><br/>                | <span data-ttu-id="d4d8f-129">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="d4d8f-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="d4d8f-130">MOF</span><span class="sxs-lookup"><span data-stu-id="d4d8f-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d4d8f-131"><dt>Тсаллов. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d4d8f-131"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="d4d8f-132">DLL</span><span class="sxs-lookup"><span data-stu-id="d4d8f-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4d8f-133"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4d8f-133"><dt>TsPubWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4d8f-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d4d8f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4d8f-135">**\_Тсекспанденвиронментвариаблес Win32**</span><span class="sxs-lookup"><span data-stu-id="d4d8f-135">**Win32\_TSExpandEnvironmentVariables**</span></span>](win32-tsexpandenvironmentvariables.md)
</dt> </dl>

 

