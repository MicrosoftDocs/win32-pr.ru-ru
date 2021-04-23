---
title: Метод Delete класса Win32_Terminal
description: Удаляет указанный терминал.
ms.assetid: 59d8cc73-aef1-49d2-a7a2-dd3cbe5a8c52
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Delete
- Службы удаленных рабочих столов метода Delete, класс Win32_Terminal
- Класс Win32_Terminal службы удаленных рабочих столов, метод Delete
topic_type:
- apiref
api_name:
- Win32_Terminal.Delete
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47b7120c78eada2b047f836219d3382e5ce1e2f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672515"
---
# <a name="delete-method-of-the-win32_terminal-class"></a><span data-ttu-id="79e80-106">Метод DELETE \_ класса терминала Win32</span><span class="sxs-lookup"><span data-stu-id="79e80-106">Delete method of the Win32\_Terminal class</span></span>

<span data-ttu-id="79e80-107">Метод **Delete** удаляет указанный терминал.</span><span class="sxs-lookup"><span data-stu-id="79e80-107">The **Delete** method deletes the specified terminal.</span></span>

## <a name="syntax"></a><span data-ttu-id="79e80-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="79e80-108">Syntax</span></span>


```mof
uint32 Delete(
  [in] string NewTerminalName
);
```



## <a name="parameters"></a><span data-ttu-id="79e80-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="79e80-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79e80-110">*Невтерминалнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="79e80-110">*NewTerminalName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79e80-111">Имя удаляемого терминала.</span><span class="sxs-lookup"><span data-stu-id="79e80-111">Name of the terminal to delete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79e80-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="79e80-112">Return value</span></span>

<span data-ttu-id="79e80-113">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="79e80-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="79e80-114">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="79e80-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="79e80-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="79e80-115">Remarks</span></span>

<span data-ttu-id="79e80-116">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="79e80-116">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="79e80-117">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="79e80-117">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="79e80-118">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="79e80-118">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="79e80-119">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="79e80-119">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="79e80-120">Требования</span><span class="sxs-lookup"><span data-stu-id="79e80-120">Requirements</span></span>



| <span data-ttu-id="79e80-121">Требование</span><span class="sxs-lookup"><span data-stu-id="79e80-121">Requirement</span></span> | <span data-ttu-id="79e80-122">Значение</span><span class="sxs-lookup"><span data-stu-id="79e80-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="79e80-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="79e80-123">Minimum supported client</span></span><br/> | <span data-ttu-id="79e80-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="79e80-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="79e80-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="79e80-125">Minimum supported server</span></span><br/> | <span data-ttu-id="79e80-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="79e80-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="79e80-127">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="79e80-127">Namespace</span></span><br/>                | <span data-ttu-id="79e80-128">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="79e80-128">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="79e80-129">MOF</span><span class="sxs-lookup"><span data-stu-id="79e80-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="79e80-130"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="79e80-130"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="79e80-131">DLL</span><span class="sxs-lookup"><span data-stu-id="79e80-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79e80-132"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79e80-132"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79e80-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="79e80-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79e80-134">**\_Терминал Win32**</span><span class="sxs-lookup"><span data-stu-id="79e80-134">**Win32\_Terminal**</span></span>](win32-terminal.md)
</dt> </dl>

 

