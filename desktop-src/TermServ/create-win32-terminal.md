---
title: Метод Create класса Win32_Terminal
description: Создает терминал с параметрами по умолчанию, которые можно настроить с помощью свойств и методов \_ классов Win32 терминалсеттинг.
ms.assetid: 64c90695-72d4-42be-a37a-89b54c04a78c
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Create
- Создание службы удаленных рабочих столов метода, Win32_Terminal класса
- Класс Win32_Terminal службы удаленных рабочих столов, метод Create
topic_type:
- apiref
api_name:
- Win32_Terminal.Create
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4f1edfa22893452f81cf4695a50380842fa5c06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489534"
---
# <a name="create-method-of-the-win32_terminal-class"></a><span data-ttu-id="3a2bb-106">Метод Create \_ класса терминала Win32</span><span class="sxs-lookup"><span data-stu-id="3a2bb-106">Create method of the Win32\_Terminal class</span></span>

<span data-ttu-id="3a2bb-107">Метод **CREATE** создает терминал с параметрами по умолчанию, которые можно настроить с помощью свойств и методов классов [**Win32 \_ терминалсеттинг**](win32-terminalsetting.md) .</span><span class="sxs-lookup"><span data-stu-id="3a2bb-107">The **Create** method creates a terminal with default settings which can be customized by using the properties and methods of the [**Win32\_TerminalSetting**](win32-terminalsetting.md) classes.</span></span> <span data-ttu-id="3a2bb-108">Функция возвращает ноль в случае успеха и ошибку при сбое.</span><span class="sxs-lookup"><span data-stu-id="3a2bb-108">The function returns zero on success and an error on failure.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a2bb-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3a2bb-109">Syntax</span></span>


```mof
uint32 Create(
  [in] string NewTerminalName,
  [in] string Transport,
  [in] string TerminalProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="3a2bb-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="3a2bb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a2bb-111">*Невтерминалнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3a2bb-111">*NewTerminalName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a2bb-112">Имя терминала.</span><span class="sxs-lookup"><span data-stu-id="3a2bb-112">Name of the terminal.</span></span>

</dd> <dt>

<span data-ttu-id="3a2bb-113">*Передача* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3a2bb-113">*Transport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a2bb-114">Транспорт для терминала.</span><span class="sxs-lookup"><span data-stu-id="3a2bb-114">Transport for the terminal.</span></span> <span data-ttu-id="3a2bb-115">Это свойство класса [**Win32 \_ тсженералсеттинг**](win32-tsgeneralsetting.md) .</span><span class="sxs-lookup"><span data-stu-id="3a2bb-115">This is a property of the [**Win32\_TSGeneralSetting**](win32-tsgeneralsetting.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="3a2bb-116">*Терминалпротокол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3a2bb-116">*TerminalProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a2bb-117">Протокол для терминала.</span><span class="sxs-lookup"><span data-stu-id="3a2bb-117">Protocol for the terminal.</span></span> <span data-ttu-id="3a2bb-118">Это свойство класса [**Win32 \_ тсженералсеттинг**](win32-tsgeneralsetting.md) .</span><span class="sxs-lookup"><span data-stu-id="3a2bb-118">This is a property of the [**Win32\_TSGeneralSetting**](win32-tsgeneralsetting.md) class.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a2bb-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3a2bb-119">Return value</span></span>

<span data-ttu-id="3a2bb-120">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="3a2bb-120">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="3a2bb-121">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="3a2bb-121">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a2bb-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3a2bb-122">Remarks</span></span>

<span data-ttu-id="3a2bb-123">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="3a2bb-123">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="3a2bb-124">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="3a2bb-124">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="3a2bb-125">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="3a2bb-125">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="3a2bb-126">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="3a2bb-126">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="3a2bb-127">Требования</span><span class="sxs-lookup"><span data-stu-id="3a2bb-127">Requirements</span></span>



| <span data-ttu-id="3a2bb-128">Требование</span><span class="sxs-lookup"><span data-stu-id="3a2bb-128">Requirement</span></span> | <span data-ttu-id="3a2bb-129">Значение</span><span class="sxs-lookup"><span data-stu-id="3a2bb-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3a2bb-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3a2bb-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3a2bb-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3a2bb-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3a2bb-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3a2bb-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3a2bb-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3a2bb-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3a2bb-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3a2bb-134">Namespace</span></span><br/>                | <span data-ttu-id="3a2bb-135">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="3a2bb-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="3a2bb-136">MOF</span><span class="sxs-lookup"><span data-stu-id="3a2bb-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3a2bb-137"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3a2bb-137"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="3a2bb-138">DLL</span><span class="sxs-lookup"><span data-stu-id="3a2bb-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a2bb-139"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a2bb-139"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a2bb-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3a2bb-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a2bb-141">**\_Терминал Win32**</span><span class="sxs-lookup"><span data-stu-id="3a2bb-141">**Win32\_Terminal**</span></span>](win32-terminal.md)
</dt> </dl>

 

