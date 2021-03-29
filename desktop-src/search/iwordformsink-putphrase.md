---
description: Помещает в объект Ивордформсинк альтернативную форму слова.
ms.assetid: 4F6A3E88-A17C-4CA3-849D-FF0DC06D5DC3
title: 'Ивордформсинк: метод:P Уталтворд (Search. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordFormSink.PutAltWord
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 43539bbf67e23bc37ca92f6a961b945ae581e746
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808920"
---
# <a name="iwordformsinkputaltword-method"></a><span data-ttu-id="d0991-103">Ивордформсинк: метод:P Уталтворд</span><span class="sxs-lookup"><span data-stu-id="d0991-103">IWordFormSink::PutAltWord method</span></span>

<span data-ttu-id="d0991-104">Помещает в объект [**ивордформсинк**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) альтернативную форму слова.</span><span class="sxs-lookup"><span data-stu-id="d0991-104">Puts an alternative form of a word in the [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0991-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d0991-105">Syntax</span></span>


```C++
HRESULT PutAltWord(
  [in] const WCHAR *pwcInBuf ,
  [in]       ULONG cwc
);
```



## <a name="parameters"></a><span data-ttu-id="d0991-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d0991-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0991-107">*пвЦинбуф* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d0991-107">*pwcInBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0991-108">Указатель на буфер, содержащий альтернативную форму слова.</span><span class="sxs-lookup"><span data-stu-id="d0991-108">A pointer to a buffer that contains an alternative form of a word.</span></span>

</dd> <dt>

<span data-ttu-id="d0991-109">*КВК* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d0991-109">*cwc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0991-110">Число символов в *пвЦинбуф*.</span><span class="sxs-lookup"><span data-stu-id="d0991-110">The number of characters in *pwcInBuf*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0991-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d0991-111">Return value</span></span>

<span data-ttu-id="d0991-112">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="d0991-112">This method can return one of these values.</span></span>



| <span data-ttu-id="d0991-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="d0991-113">Return code</span></span>                                                                                              | <span data-ttu-id="d0991-114">Описание</span><span class="sxs-lookup"><span data-stu-id="d0991-114">Description</span></span>                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d0991-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="d0991-115"><dt>**S\_OK**</dt></span></span> </dl>                     | <span data-ttu-id="d0991-116">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="d0991-116">The operation was completed successfully.</span></span> <br/>                                                                                             |
| <dl> <span data-ttu-id="d0991-117"><dt>**Языковая \_ \_крупное \_ слово S**</dt></span><span class="sxs-lookup"><span data-stu-id="d0991-117"><dt>**LANGUAGE\_S\_LARGE\_WORD** </dt></span></span> </dl> | <span data-ttu-id="d0991-118">Значение *КВК* больше, чем значение *улмакстокенсизе* , указанное в [**истеммер:: init**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-init).</span><span class="sxs-lookup"><span data-stu-id="d0991-118">Value of *cwc* is larger than the value for *ulMaxTokenSize* that is specified in [**IStemmer::Init**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-init).</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="d0991-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d0991-119">Remarks</span></span>

<span data-ttu-id="d0991-120">Этот метод вызывается из метода [**женератевордформс**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-generatewordforms) реализации [**истеммер**](/windows/win32/api/indexsrv/nn-indexsrv-istemmer) .</span><span class="sxs-lookup"><span data-stu-id="d0991-120">This method is called from the [**GenerateWordForms**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-generatewordforms) method of the [**IStemmer**](/windows/win32/api/indexsrv/nn-indexsrv-istemmer) implementation.</span></span> <span data-ttu-id="d0991-121">Все альтернативные формы для слова, за исключением последнего, помещаются в объект [**ивордформсинк**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) путем вызова **Ивордформсинк::P уталтворд**.</span><span class="sxs-lookup"><span data-stu-id="d0991-121">All alternative forms for a word, except the last, are put in the [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) object by calling **IWordFormSink::PutAltWord**.</span></span> <span data-ttu-id="d0991-122">Последняя альтернативная форма слова, которая всегда является исходной формой слова, обрабатывается путем вызова [**ивордформсинк::P утворд**](iwordformsink-putword.md).</span><span class="sxs-lookup"><span data-stu-id="d0991-122">The final alternative form of a word, which is always the original form of the word, is handled by calling [**IWordFormSink::PutWord**](iwordformsink-putword.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d0991-123">Требования</span><span class="sxs-lookup"><span data-stu-id="d0991-123">Requirements</span></span>



| <span data-ttu-id="d0991-124">Требование</span><span class="sxs-lookup"><span data-stu-id="d0991-124">Requirement</span></span> | <span data-ttu-id="d0991-125">Значение</span><span class="sxs-lookup"><span data-stu-id="d0991-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d0991-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d0991-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d0991-127">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d0991-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="d0991-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d0991-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d0991-129">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d0991-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d0991-130">Заголовок</span><span class="sxs-lookup"><span data-stu-id="d0991-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0991-131"><dt>Поиск. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0991-131"><dt>Search.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0991-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d0991-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0991-133">**ивордформсинк**</span><span class="sxs-lookup"><span data-stu-id="d0991-133">**IWordFormSink**</span></span>](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink)
</dt> </dl>

 

 
