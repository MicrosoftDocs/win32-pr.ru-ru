---
title: Метод Инитиалпрограм класса Win32_TSEnvironmentSetting
description: Метод Инитиалпрограм задает свойства программы запуска, такие как имя, Рабочий каталог и путь программы, которые должны запускаться сразу после входа на сервер узла сеансов удаленный рабочий стол (узел сеансов удаленных рабочих столов).
ms.assetid: e53621cf-ade8-4301-acc0-232866e88488
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Инитиалпрограм
- Службы удаленных рабочих столов метода Инитиалпрограм, класс Win32_TSEnvironmentSetting
- Класс Win32_TSEnvironmentSetting службы удаленных рабочих столов, метод Инитиалпрограм
topic_type:
- apiref
api_name:
- Win32_TSEnvironmentSetting.InitialProgram
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccd41e1af990e37b8458431106bc2ec9a8489b14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681868"
---
# <a name="initialprogram-method-of-the-win32_tsenvironmentsetting-class"></a><span data-ttu-id="1b582-106">Метод Инитиалпрограм \_ класса Win32 тсенвиронментсеттинг</span><span class="sxs-lookup"><span data-stu-id="1b582-106">InitialProgram method of the Win32\_TSEnvironmentSetting class</span></span>

<span data-ttu-id="1b582-107">Метод **инитиалпрограм** задает свойства программы запуска, такие как имя, Рабочий каталог и путь программы, которые должны запускаться сразу после входа на сервер узла сеансов удаленный рабочий стол (узел сеансов удаленных рабочих столов).</span><span class="sxs-lookup"><span data-stu-id="1b582-107">The **InitialProgram** method sets startup program properties such as the name, working directory, and path of the program to start immediately after logon to the Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b582-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1b582-108">Syntax</span></span>


```mof
uint32 InitialProgram(
  [in] string InitialProgramPath,
  [in] string Startin
);
```



## <a name="parameters"></a><span data-ttu-id="1b582-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="1b582-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b582-110">*Инитиалпрогрампас* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1b582-110">*InitialProgramPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b582-111">Имя и путь к программе запуска.</span><span class="sxs-lookup"><span data-stu-id="1b582-111">The name and path of the startup program.</span></span>

</dd> <dt>

<span data-ttu-id="1b582-112">*Запуск* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1b582-112">*Startin* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b582-113">Путь к рабочему каталогу программы запуска.</span><span class="sxs-lookup"><span data-stu-id="1b582-113">The path to the working directory of the startup program.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b582-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1b582-114">Return value</span></span>

<span data-ttu-id="1b582-115">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="1b582-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="1b582-116">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="1b582-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="1b582-117">Метод возвращает ошибку, если параметр находится в разделе Управление групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="1b582-117">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b582-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1b582-118">Remarks</span></span>

<span data-ttu-id="1b582-119">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="1b582-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1b582-120">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="1b582-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="1b582-121">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="1b582-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1b582-122">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="1b582-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="1b582-123">Требования</span><span class="sxs-lookup"><span data-stu-id="1b582-123">Requirements</span></span>



| <span data-ttu-id="1b582-124">Требование</span><span class="sxs-lookup"><span data-stu-id="1b582-124">Requirement</span></span> | <span data-ttu-id="1b582-125">Значение</span><span class="sxs-lookup"><span data-stu-id="1b582-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1b582-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1b582-126">Minimum supported client</span></span><br/> | <span data-ttu-id="1b582-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1b582-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1b582-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1b582-128">Minimum supported server</span></span><br/> | <span data-ttu-id="1b582-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1b582-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1b582-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1b582-130">Namespace</span></span><br/>                | <span data-ttu-id="1b582-131">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="1b582-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="1b582-132">MOF</span><span class="sxs-lookup"><span data-stu-id="1b582-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1b582-133"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1b582-133"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="1b582-134">DLL</span><span class="sxs-lookup"><span data-stu-id="1b582-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b582-135"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b582-135"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b582-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1b582-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b582-137">**\_Тсенвиронментсеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="1b582-137">**Win32\_TSEnvironmentSetting**</span></span>](win32-tsenvironmentsetting.md)
</dt> </dl>

 

