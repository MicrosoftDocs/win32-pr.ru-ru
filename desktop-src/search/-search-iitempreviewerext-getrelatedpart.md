---
description: Возвращает связанную часть тела для внедрения в выходной поток MHTML.
ms.assetid: 7810568b-5fb7-4814-aa9f-d7ae805c97e1
title: 'Метод Иитемпревиеверекст:: Жетрелатедпарт'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt.GetRelatedPart
api_type:
- COM
api_location: ''
ms.openlocfilehash: 281d91b1679b2a944996bb1c85060d16c4e0b966
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710923"
---
# <a name="iitempreviewerextgetrelatedpart-method"></a><span data-ttu-id="bb369-103">Метод Иитемпревиеверекст:: Жетрелатедпарт</span><span class="sxs-lookup"><span data-stu-id="bb369-103">IItemPreviewerExt::GetRelatedPart method</span></span>

<span data-ttu-id="bb369-104">Возвращает связанную часть тела для внедрения в выходной поток MHTML.</span><span class="sxs-lookup"><span data-stu-id="bb369-104">Gets a related body part for embedding into the output MHTML stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb369-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bb369-105">Syntax</span></span>


```C++
HRESULT GetRelatedPart(
  [in]          DWORD     dwContext,
  [in]          LPCOLESTR pwszProp,
  [in]          DWORD     dwIndex,
  [out, retval] LINKINFO  *pInfo
);
```



## <a name="parameters"></a><span data-ttu-id="bb369-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bb369-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb369-107">*двконтекст* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bb369-107">*dwContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb369-108">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="bb369-108">Type: **DWORD**</span></span>

<span data-ttu-id="bb369-109">Идентификатор контекста для операции.</span><span class="sxs-lookup"><span data-stu-id="bb369-109">The context identifier for the operation.</span></span> <span data-ttu-id="bb369-110">Переопределите **двконтекст** по умолчанию, чтобы задать для идентификатора контекста значение, выбранное вами.</span><span class="sxs-lookup"><span data-stu-id="bb369-110">Override the **dwContext** default to set the context identifier to a value of your choosing.</span></span>

</dd> <dt>

<span data-ttu-id="bb369-111">*пвсзпроп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bb369-111">*pwszProp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb369-112">Тип: **лпколестр**</span><span class="sxs-lookup"><span data-stu-id="bb369-112">Type: **LPCOLESTR**</span></span>

<span data-ttu-id="bb369-113">Указатель на свойство связанного содержимого в виде строки в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="bb369-113">A pointer to the property of the linked content as a Unicode string.</span></span>

</dd> <dt>

<span data-ttu-id="bb369-114">*двиндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bb369-114">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb369-115">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="bb369-115">Type: **DWORD**</span></span>

<span data-ttu-id="bb369-116">Длинное целое число без знака, содержащее Отсчитываемый от нуля индекс связанной части тела.</span><span class="sxs-lookup"><span data-stu-id="bb369-116">An unsigned long integer value that contains the zero-based index of the related body part.</span></span>

</dd> <dt>

<span data-ttu-id="bb369-117">*пинфо* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="bb369-117">*pInfo* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="bb369-118">Тип: \**[**линкинфо**](-search-linkinfo.md) \** _</span><span class="sxs-lookup"><span data-stu-id="bb369-118">Type: \**[**LINKINFO**](-search-linkinfo.md)\** _</span></span>

<span data-ttu-id="bb369-119">Получает указатель на структуру [_ *линкинфо* \*](-search-linkinfo.md) , в которой метод возвращает сведения о транзакции.</span><span class="sxs-lookup"><span data-stu-id="bb369-119">Receives a pointer to the [_ *LINKINFO*\*](-search-linkinfo.md) structure in which the method returns information about the transaction.</span></span> <span data-ttu-id="bb369-120">*пинфо* не должен быть **пустым** указателем.</span><span class="sxs-lookup"><span data-stu-id="bb369-120">*pInfo* must not be a **NULL** pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb369-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bb369-121">Return value</span></span>

<span data-ttu-id="bb369-122">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="bb369-122">Type: **HRESULT**</span></span>

<span data-ttu-id="bb369-123">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="bb369-123">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bb369-124">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bb369-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb369-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bb369-125">Remarks</span></span>

<span data-ttu-id="bb369-126">Интерфейс [**иитемпревиеверекст**](-search-iitempreviewerext.md) поддерживается только в Windows XP и windows Server 2003 и больше не должен использоваться.</span><span class="sxs-lookup"><span data-stu-id="bb369-126">The [**IItemPreviewerExt**](-search-iitempreviewerext.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="bb369-127">Для предварительного просмотра вложений с помощью обработчика протоколов стороннего производителя на компьютерах под управлением Windows XP или Windows Server 2003 может потребоваться использовать интерфейс [**иитемпревиеверекст**](-search-iitempreviewerext.md) и следующие API: интерфейсы [**исеарчпротоколуи**](-search-isearchprotocolui.md), [**Иитемпропертибаг**](iitempropertybag.md) и [**исеарчитем**](-search-isearchitem.md) , структура [**линкинфо**](-search-linkinfo.md) и [**перечисление**](-search-linktype.md) типов ссылок.</span><span class="sxs-lookup"><span data-stu-id="bb369-127">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the [**IItemPreviewerExt**](-search-iitempreviewerext.md) interface, and the following APIs: the [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) structure, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb369-128">Требования</span><span class="sxs-lookup"><span data-stu-id="bb369-128">Requirements</span></span>



| <span data-ttu-id="bb369-129">Требование</span><span class="sxs-lookup"><span data-stu-id="bb369-129">Requirement</span></span> | <span data-ttu-id="bb369-130">Значение</span><span class="sxs-lookup"><span data-stu-id="bb369-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bb369-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bb369-131">Minimum supported client</span></span><br/> | <span data-ttu-id="bb369-132">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="bb369-132">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="bb369-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bb369-133">Minimum supported server</span></span><br/> | <span data-ttu-id="bb369-134">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bb369-134">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="bb369-135">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="bb369-135">Redistributable</span></span><br/>          | <span data-ttu-id="bb369-136">Поиск на рабочем столе Windows (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="bb369-136">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="bb369-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bb369-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb369-138">**иитемпревиеверекст**</span><span class="sxs-lookup"><span data-stu-id="bb369-138">**IItemPreviewerExt**</span></span>](-search-iitempreviewerext.md)
</dt> </dl>

 

 




