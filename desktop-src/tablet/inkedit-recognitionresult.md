---
description: 'Происходит, когда элемент управления InkEdit получает результаты вручную из вызова метода InkEdit:: Recognize или автоматически после срабатывания времени ожидания распознавания.'
ms.assetid: 09618be0-fe49-494f-940f-79ff8352097e
title: Событие InkEdit. Рекогнитионресулт (with. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40d6206293b604e5540b5e6d0271e1ebe984a987
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272317"
---
# <a name="inkeditrecognitionresult-event"></a><span data-ttu-id="9104b-103">Событие InkEdit. Рекогнитионресулт</span><span class="sxs-lookup"><span data-stu-id="9104b-103">InkEdit.RecognitionResult event</span></span>

<span data-ttu-id="9104b-104">Происходит, когда элемент управления [InkEdit](inkedit-control-reference.md) получает результаты вручную из вызова метода [**InkEdit:: Recognize**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) или автоматически после срабатывания времени ожидания распознавания.</span><span class="sxs-lookup"><span data-stu-id="9104b-104">Occurs when the [InkEdit](inkedit-control-reference.md) control gets results manually from a call to the [**InkEdit::Recognize**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) method or automatically after the recognition timeout fires.</span></span>

## <a name="syntax"></a><span data-ttu-id="9104b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9104b-105">Syntax</span></span>


```C++
void RecognitionResult(
  [in] IInkRecognitionResult *RecognitionResult
);
```



## <a name="parameters"></a><span data-ttu-id="9104b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9104b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9104b-107">*Рекогнитионресулт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9104b-107">*RecognitionResult* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9104b-108">Объект [**иинкрекогнитионресулт**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) , содержащий результат распознавания.</span><span class="sxs-lookup"><span data-stu-id="9104b-108">An [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) object that contains the result of the recognition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9104b-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9104b-109">Return value</span></span>

<span data-ttu-id="9104b-110">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="9104b-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9104b-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9104b-111">Remarks</span></span>

<span data-ttu-id="9104b-112">Этот метод события определен в интерфейсе **\_ иинкедитевентс** .</span><span class="sxs-lookup"><span data-stu-id="9104b-112">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="9104b-113">Интерфейс **\_ иинкедитевентс** реализует интерфейс [**IDISPATCH**](/windows/win32/api/oaidl/nn-oaidl-idispatch) с идентификатором DISPID \_ иирекогнитионресулт.</span><span class="sxs-lookup"><span data-stu-id="9104b-113">The **\_IInkEditEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IeeRecognitionResult.</span></span>

## <a name="requirements"></a><span data-ttu-id="9104b-114">Требования</span><span class="sxs-lookup"><span data-stu-id="9104b-114">Requirements</span></span>



| <span data-ttu-id="9104b-115">Требование</span><span class="sxs-lookup"><span data-stu-id="9104b-115">Requirement</span></span> | <span data-ttu-id="9104b-116">Значение</span><span class="sxs-lookup"><span data-stu-id="9104b-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9104b-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9104b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9104b-118">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="9104b-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9104b-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9104b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9104b-120">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="9104b-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="9104b-121">Header</span><span class="sxs-lookup"><span data-stu-id="9104b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="9104b-122"><dt>«С». h (также требует \_ ввода i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="9104b-122"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="9104b-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9104b-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="9104b-124"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9104b-124"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="9104b-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9104b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9104b-126">InkEdit</span><span class="sxs-lookup"><span data-stu-id="9104b-126">InkEdit</span></span>](inkedit-control-reference.md)
</dt> <dt>

<span data-ttu-id="9104b-127">[**Recognize \[ элемент управления InkEdit метода\]**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize)</span><span class="sxs-lookup"><span data-stu-id="9104b-127">[**Recognize Method \[InkEdit Control\]**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize)</span></span>
</dt> </dl>

 

