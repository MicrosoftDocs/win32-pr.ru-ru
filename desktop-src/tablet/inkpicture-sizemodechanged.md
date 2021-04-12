---
description: Происходит после изменения свойства Сиземоде элемента управления InkPicture.
ms.assetid: ae56b5a2-e3e2-468c-a572-a9b46eb1d39d
title: Событие InkPicture. Сиземодечанжед (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f270ea141bc8803cbcf1ce4e54b0f73318ed69d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348655"
---
# <a name="inkpicturesizemodechanged-event"></a><span data-ttu-id="34925-103">Событие InkPicture. Сиземодечанжед</span><span class="sxs-lookup"><span data-stu-id="34925-103">InkPicture.SizeModeChanged event</span></span>

<span data-ttu-id="34925-104">Происходит после изменения свойства [**сиземоде**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) элемента управления [InkPicture](inkpicture-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="34925-104">Occurs after the [**SizeMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) property of the [InkPicture](inkpicture-control-reference.md) control has been changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="34925-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="34925-105">Syntax</span></span>


```C++
void SizeModeChanged(
  [in] InkPictureSizeMode NewMode,
  [in] InkPictureSizeMode OldMode
);
```



## <a name="parameters"></a><span data-ttu-id="34925-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="34925-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34925-107">*Использованием NewMode* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="34925-107">*NewMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34925-108">Новое состояние элемента управления [InkPicture](inkpicture-control-reference.md) на основе нового значения свойства [**сиземоде**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) .</span><span class="sxs-lookup"><span data-stu-id="34925-108">The new state of the [InkPicture](inkpicture-control-reference.md) control, based on the new value of the [**SizeMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) property.</span></span>

</dd> <dt>

<span data-ttu-id="34925-109">*Олдмоде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="34925-109">*OldMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34925-110">Старое состояние элемента управления [InkPicture](inkpicture-control-reference.md) , основанное на старом значении свойства [**сиземоде**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) .</span><span class="sxs-lookup"><span data-stu-id="34925-110">The old state of the [InkPicture](inkpicture-control-reference.md) control, based on the old value of the [**SizeMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34925-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="34925-111">Return value</span></span>

<span data-ttu-id="34925-112">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="34925-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="34925-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="34925-113">Remarks</span></span>

<span data-ttu-id="34925-114">Этот метод события определен в интерфейсе **\_ иинкпиктуривентс** .</span><span class="sxs-lookup"><span data-stu-id="34925-114">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="34925-115">Интерфейс **\_ иинкпиктуривентс** реализует интерфейс [**IDISPATCH**](/windows/win32/api/oaidl/nn-oaidl-idispatch) с идентификатором DISPID \_ ипесиземодечанжед.</span><span class="sxs-lookup"><span data-stu-id="34925-115">The **\_IInkPictureEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IPESizeModeChanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="34925-116">Требования</span><span class="sxs-lookup"><span data-stu-id="34925-116">Requirements</span></span>



| <span data-ttu-id="34925-117">Требование</span><span class="sxs-lookup"><span data-stu-id="34925-117">Requirement</span></span> | <span data-ttu-id="34925-118">Значение</span><span class="sxs-lookup"><span data-stu-id="34925-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34925-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="34925-119">Minimum supported client</span></span><br/> | <span data-ttu-id="34925-120">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="34925-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="34925-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="34925-121">Minimum supported server</span></span><br/> | <span data-ttu-id="34925-122">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="34925-122">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="34925-123">Header</span><span class="sxs-lookup"><span data-stu-id="34925-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="34925-124"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="34925-124"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="34925-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="34925-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="34925-126"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34925-126"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="34925-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="34925-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34925-128">InkPicture</span><span class="sxs-lookup"><span data-stu-id="34925-128">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

