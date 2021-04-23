---
description: Сбрасывает виртуальную клавиатуру.
ms.assetid: 6D4A9F02-53BD-47C2-9C09-F22C3630312F
title: Метод Reset класса Msvm_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.Reset
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4fe46657177789e49b49ec2c36f0e7a9dc95394f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664513"
---
# <a name="reset-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="866ec-103">Метод Reset \_ класса мсвм Keyboard</span><span class="sxs-lookup"><span data-stu-id="866ec-103">Reset method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="866ec-104">Сбрасывает виртуальную клавиатуру.</span><span class="sxs-lookup"><span data-stu-id="866ec-104">Resets the virtual keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="866ec-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="866ec-105">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="866ec-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="866ec-106">Parameters</span></span>

<span data-ttu-id="866ec-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="866ec-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="866ec-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="866ec-108">Return value</span></span>

<span data-ttu-id="866ec-109">Возвращаемое значение, равное нулю, указывает на успешное выполнение.</span><span class="sxs-lookup"><span data-stu-id="866ec-109">A return value of zero indicates success.</span></span> <span data-ttu-id="866ec-110">Возвращаемое значение, равное единице, указывает на сбой, так как метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="866ec-110">A return value of one indicates a failure because the method is not supported.</span></span>

<dl> <dt>

<span data-ttu-id="866ec-111">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="866ec-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="866ec-112">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="866ec-112">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="866ec-113">Требования</span><span class="sxs-lookup"><span data-stu-id="866ec-113">Requirements</span></span>



| <span data-ttu-id="866ec-114">Требование</span><span class="sxs-lookup"><span data-stu-id="866ec-114">Requirement</span></span> | <span data-ttu-id="866ec-115">Значение</span><span class="sxs-lookup"><span data-stu-id="866ec-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="866ec-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="866ec-116">Minimum supported client</span></span><br/> | <span data-ttu-id="866ec-117">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="866ec-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="866ec-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="866ec-118">Minimum supported server</span></span><br/> | <span data-ttu-id="866ec-119">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="866ec-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="866ec-120">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="866ec-120">Namespace</span></span><br/>                | <span data-ttu-id="866ec-121">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="866ec-121">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="866ec-122">MOF</span><span class="sxs-lookup"><span data-stu-id="866ec-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="866ec-123"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="866ec-123"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="866ec-124">DLL</span><span class="sxs-lookup"><span data-stu-id="866ec-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="866ec-125"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="866ec-125"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="866ec-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="866ec-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="866ec-127">**Мсвм \_ клавиатура**</span><span class="sxs-lookup"><span data-stu-id="866ec-127">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> </dl>

 

 




