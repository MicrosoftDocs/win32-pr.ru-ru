---
description: Помещает исходную форму Word в объект Ивордформсинк.
ms.assetid: 333A3109-6C0A-42AE-9E10-87F53C7F737C
title: 'Ивордформсинк: метод:P Утворд (Search. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordFormSink.PutWord
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 438cb41e50f264bd373ae2ef8e84598b651b0352
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692185"
---
# <a name="iwordformsinkputword-method"></a><span data-ttu-id="2173b-103">Ивордформсинк: метод:P Утворд</span><span class="sxs-lookup"><span data-stu-id="2173b-103">IWordFormSink::PutWord method</span></span>

<span data-ttu-id="2173b-104">Помещает исходную форму Word в объект [**ивордформсинк**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) .</span><span class="sxs-lookup"><span data-stu-id="2173b-104">Puts the original word form in the [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="2173b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2173b-105">Syntax</span></span>


```C++
HRESULT PutWord(
  [in] const WCHAR *pwcInBuf ,
  [in]       ULONG cwc
);
```



## <a name="parameters"></a><span data-ttu-id="2173b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2173b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2173b-107">*пвЦинбуф* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2173b-107">*pwcInBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2173b-108">Указатель на буфер, содержащий последнюю альтернативную форму слова, которое всегда является исходным словом.</span><span class="sxs-lookup"><span data-stu-id="2173b-108">A pointer to a buffer that contains the final alternative form of a word, which is always the original word.</span></span>

</dd> <dt>

<span data-ttu-id="2173b-109">*КВК* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2173b-109">*cwc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2173b-110">Число символов в *пвЦинбуф*.</span><span class="sxs-lookup"><span data-stu-id="2173b-110">The number of characters in *pwcInBuf*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2173b-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2173b-111">Return value</span></span>

<span data-ttu-id="2173b-112">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="2173b-112">This method can return one of these values.</span></span>



| <span data-ttu-id="2173b-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="2173b-113">Return code</span></span>                                                                          | <span data-ttu-id="2173b-114">Описание</span><span class="sxs-lookup"><span data-stu-id="2173b-114">Description</span></span>                                           |
|--------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="2173b-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="2173b-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="2173b-116">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="2173b-116">The operation was completed successfully.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="2173b-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2173b-117">Remarks</span></span>

<span data-ttu-id="2173b-118">**Путворд** вызывается из метода [**женератевордформс**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-generatewordforms) реализации [**истеммер**](/windows/win32/api/indexsrv/nn-indexsrv-istemmer) .</span><span class="sxs-lookup"><span data-stu-id="2173b-118">**PutWord** is called from the [**GenerateWordForms**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-generatewordforms) method of the [**IStemmer**](/windows/win32/api/indexsrv/nn-indexsrv-istemmer) implementation.</span></span> <span data-ttu-id="2173b-119">Этот метод обрабатывает исходную форму слова и вызывается последним.</span><span class="sxs-lookup"><span data-stu-id="2173b-119">This method handles the original form of a word and is called last.</span></span> <span data-ttu-id="2173b-120">Все предыдущие формы для слова помещаются в объект [**ивордформсинк**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) путем вызова [**Ивордформсинк::P уталтворд**](iwordformsink-putphrase.md).</span><span class="sxs-lookup"><span data-stu-id="2173b-120">All preceding alternative forms for a word are put in the [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) object by calling [**IWordFormSink::PutAltWord**](iwordformsink-putphrase.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2173b-121">Требования</span><span class="sxs-lookup"><span data-stu-id="2173b-121">Requirements</span></span>



| <span data-ttu-id="2173b-122">Требование</span><span class="sxs-lookup"><span data-stu-id="2173b-122">Requirement</span></span> | <span data-ttu-id="2173b-123">Значение</span><span class="sxs-lookup"><span data-stu-id="2173b-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2173b-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2173b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2173b-125">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2173b-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="2173b-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2173b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2173b-127">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2173b-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="2173b-128">Заголовок</span><span class="sxs-lookup"><span data-stu-id="2173b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="2173b-129"><dt>Поиск. h</dt></span><span class="sxs-lookup"><span data-stu-id="2173b-129"><dt>Search.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2173b-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2173b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2173b-131">**ивордформсинк**</span><span class="sxs-lookup"><span data-stu-id="2173b-131">**IWordFormSink**</span></span>](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink)
</dt> </dl>

 

 
