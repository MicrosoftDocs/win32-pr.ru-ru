---
description: Пытается отправить определяемый пользователем код элемента управления службе, управляемой драйвером системы.
ms.assetid: 62e66c35-f264-43d0-9e94-fb5e85f936e0
ms.tgt_platform: multiple
title: Метод Усерконтролсервице класса Win32_SystemDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.UserControlService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 99974206f6487d90e1660f5a64c1d00904912c66
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990736"
---
# <a name="usercontrolservice-method-of-the-win32_systemdriver-class"></a><span data-ttu-id="cb5db-103">Метод Усерконтролсервице \_ класса Win32 SystemDriver</span><span class="sxs-lookup"><span data-stu-id="cb5db-103">UserControlService method of the Win32\_SystemDriver class</span></span>

<span data-ttu-id="cb5db-104">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) усерконтролсервице пытается отправить определяемый пользователем код элемента управления службе, управляемой драйвером системы.</span><span class="sxs-lookup"><span data-stu-id="cb5db-104">The **UserControlService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to send a user-defined control code to a service managed by a system driver.</span></span>

<span data-ttu-id="cb5db-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="cb5db-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="cb5db-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="cb5db-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="cb5db-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cb5db-107">Syntax</span></span>


```mof
uint32 UserControlService(
  [in] uint8 ControlCode
);
```



## <a name="parameters"></a><span data-ttu-id="cb5db-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="cb5db-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb5db-109">*Контролкоде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cb5db-109">*ControlCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb5db-110">Задает определенные значения (от 128 до 255), которые предоставляют управляющие команды, характерные для пользователя.</span><span class="sxs-lookup"><span data-stu-id="cb5db-110">Specifies defined values (from 128 to 255) that provide control commands specific to a user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb5db-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cb5db-111">Return value</span></span>

<span data-ttu-id="cb5db-112">Возвращает значение 0 (ноль), если запрос **усерконтролсервице** был принят, 1 (один), если запрос не поддерживается, и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="cb5db-112">Returns a value of 0 (zero) if the **UserControlService** request was accepted, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb5db-113">Требования</span><span class="sxs-lookup"><span data-stu-id="cb5db-113">Requirements</span></span>



| <span data-ttu-id="cb5db-114">Требование</span><span class="sxs-lookup"><span data-stu-id="cb5db-114">Requirement</span></span> | <span data-ttu-id="cb5db-115">Значение</span><span class="sxs-lookup"><span data-stu-id="cb5db-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cb5db-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cb5db-116">Minimum supported client</span></span><br/> | <span data-ttu-id="cb5db-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cb5db-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cb5db-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cb5db-118">Minimum supported server</span></span><br/> | <span data-ttu-id="cb5db-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cb5db-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cb5db-120">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="cb5db-120">Namespace</span></span><br/>                | <span data-ttu-id="cb5db-121">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="cb5db-121">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cb5db-122">MOF</span><span class="sxs-lookup"><span data-stu-id="cb5db-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cb5db-123"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cb5db-123"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cb5db-124">DLL</span><span class="sxs-lookup"><span data-stu-id="cb5db-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb5db-125"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb5db-125"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb5db-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cb5db-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="cb5db-127">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cb5db-127">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="cb5db-128">**\_SystemDriver Win32**</span><span class="sxs-lookup"><span data-stu-id="cb5db-128">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)
</dt> </dl>

 

