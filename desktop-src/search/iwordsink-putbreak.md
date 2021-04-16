---
description: Помещает разрыв после предыдущего слова.
ms.assetid: C8622067-D8CE-4099-8B9F-941720F4706B
title: 'Ивордсинк: метод:P Утбреак (Search. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.PutBreak
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: c6407f1307b4860960c5202af13de736c7921139
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342932"
---
# <a name="iwordsinkputbreak-method"></a><span data-ttu-id="43190-103">Ивордсинк: метод:P Утбреак</span><span class="sxs-lookup"><span data-stu-id="43190-103">IWordSink::PutBreak method</span></span>

<span data-ttu-id="43190-104">Помещает разрыв после предыдущего слова.</span><span class="sxs-lookup"><span data-stu-id="43190-104">Puts a break after the preceding word.</span></span>

## <a name="syntax"></a><span data-ttu-id="43190-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="43190-105">Syntax</span></span>


```C++
HRESULT PutBreak(
  [in] WORDREP_BREAK_TYPE breakType
);
```



## <a name="parameters"></a><span data-ttu-id="43190-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="43190-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43190-107">*бреактипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="43190-107">*breakType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43190-108">Значение из [**\_ \_ типа разрыва вордреп**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85)) , указывающее тип разрыва, который вордсинк вставляет после предыдущего слова.</span><span class="sxs-lookup"><span data-stu-id="43190-108">A value from [**WORDREP\_BREAK\_TYPE**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85)) that indicates the type of break that the WordSink inserts after the preceding word.</span></span> <span data-ttu-id="43190-109">Каждый останов занимает уникальную точку в индексе.</span><span class="sxs-lookup"><span data-stu-id="43190-109">Each break occupies a unique position in the index.</span></span> <span data-ttu-id="43190-110">Поэтому при вставке разрывов между словами изменяется относительное расстояние между словами.</span><span class="sxs-lookup"><span data-stu-id="43190-110">Therefore, inserting breaks between words changes the relative distance between words.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43190-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="43190-111">Return value</span></span>

<span data-ttu-id="43190-112">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="43190-112">This method can return one of these values.</span></span>



| <span data-ttu-id="43190-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="43190-113">Return code</span></span>                                                                          | <span data-ttu-id="43190-114">Описание</span><span class="sxs-lookup"><span data-stu-id="43190-114">Description</span></span>                                          |
|--------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="43190-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="43190-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="43190-116">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="43190-116">The operation was completed successfully.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="43190-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="43190-117">Remarks</span></span>

<span data-ttu-id="43190-118">Методы [**ивордсинкпутворд**](iwordsink-putword.md) и [**Ивордсинк::P уталтворд**](iwordsink-putaltword.md) автоматически вставляют разрыв конца слова (Еов, обозначенный \_ элементом вордреп Break \_ Еов в перечислимом типе [**вордреп \_ \_ break**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85)) ) после каждого слова.</span><span class="sxs-lookup"><span data-stu-id="43190-118">The [**IWordSinkPutWord**](iwordsink-putword.md) and [**IWordSink::PutAltWord**](iwordsink-putaltword.md) methods automatically insert an end-of-word break (EOW, indicated by the WORDREP\_BREAK\_EOW element of the [**WORDREP\_BREAK\_TYPE**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85)) enumerated type) after each word.</span></span> <span data-ttu-id="43190-119">Вызовите метод **путбреак** , чтобы вставить тип разрыва, отличный от конца слова.</span><span class="sxs-lookup"><span data-stu-id="43190-119">Call the **PutBreak** method to insert a break type other than end of word.</span></span> <span data-ttu-id="43190-120">Этот метод не изменяет исходный текстовый буфер (*псаурцетекст*) или не увеличивает число символов (*КВК*).</span><span class="sxs-lookup"><span data-stu-id="43190-120">This method does not change the source text buffer (*pSourceText*) or increment the character count (*cwc*).</span></span> <span data-ttu-id="43190-121">Однако он увеличивает текущую позиции в индексе и влияет на результаты запроса.</span><span class="sxs-lookup"><span data-stu-id="43190-121">However, it does increment the current position in the index and affects query results.</span></span>

## <a name="requirements"></a><span data-ttu-id="43190-122">Требования</span><span class="sxs-lookup"><span data-stu-id="43190-122">Requirements</span></span>



| <span data-ttu-id="43190-123">Требование</span><span class="sxs-lookup"><span data-stu-id="43190-123">Requirement</span></span> | <span data-ttu-id="43190-124">Значение</span><span class="sxs-lookup"><span data-stu-id="43190-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="43190-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="43190-125">Minimum supported client</span></span><br/> | <span data-ttu-id="43190-126">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="43190-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="43190-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="43190-127">Minimum supported server</span></span><br/> | <span data-ttu-id="43190-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="43190-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="43190-129">Заголовок</span><span class="sxs-lookup"><span data-stu-id="43190-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="43190-130"><dt>Поиск. h</dt></span><span class="sxs-lookup"><span data-stu-id="43190-130"><dt>Search.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43190-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="43190-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43190-132">**ивордсинк**</span><span class="sxs-lookup"><span data-stu-id="43190-132">**IWordSink**</span></span>](iwordsink.md)
</dt> </dl>

 

 
