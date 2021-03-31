---
description: Возвращает элемент поиска для указанных данных. Этот метод вызывается один раз для каждого URL-адреса, обрабатываемого средством сбора данных, и получает указатель на объект Исеарчитем.
ms.assetid: 35893bc9-8327-44f9-a9fc-7855c5c063e3
title: 'Метод Исеарчпротоколуи:: Жетсеарчитемфорурл'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchProtocolUI.GetSearchItemForUrl
api_type:
- COM
api_location: ''
ms.openlocfilehash: f8a9bbe3459109946b7a4789d9b9f0fb7473ff05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808950"
---
# <a name="isearchprotocoluigetsearchitemforurl-method"></a><span data-ttu-id="cec49-104">Метод Исеарчпротоколуи:: Жетсеарчитемфорурл</span><span class="sxs-lookup"><span data-stu-id="cec49-104">ISearchProtocolUI::GetSearchItemForUrl method</span></span>

<span data-ttu-id="cec49-105">Возвращает элемент поиска для указанных данных.</span><span class="sxs-lookup"><span data-stu-id="cec49-105">Gets the search item for the data specified.</span></span> <span data-ttu-id="cec49-106">Этот метод вызывается один раз для каждого URL-адреса, обрабатываемого средством сбора данных, и получает указатель на объект [**исеарчитем**](-search-isearchitem.md) .</span><span class="sxs-lookup"><span data-stu-id="cec49-106">This method is called once for every URL processed by the gatherer, and retrieves a pointer to the [**ISearchItem**](-search-isearchitem.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="cec49-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cec49-107">Syntax</span></span>


```C++
HRESULT GetSearchItemForUrl(
  [in]          LPCOLESTR        pcwszURL,
  [in]          IItemPropertyBag *pPropertyBag,
  [out, retval] ISearchItem      **ppSearchItem
);
```



## <a name="parameters"></a><span data-ttu-id="cec49-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="cec49-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cec49-109">*пквсзурл* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cec49-109">*pcwszURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cec49-110">Тип: **лпколестр**</span><span class="sxs-lookup"><span data-stu-id="cec49-110">Type: **LPCOLESTR**</span></span>

<span data-ttu-id="cec49-111">Указатель на пустую строку данных в Юникоде, содержащую элемент поиска для URL-адреса, к которому осуществляется доступ.</span><span class="sxs-lookup"><span data-stu-id="cec49-111">Pointer to a null data terminated Unicode string containing the search item for the URL being accessed.</span></span>

</dd> <dt>

<span data-ttu-id="cec49-112">*ппропертибаг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cec49-112">*pPropertyBag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cec49-113">Тип: \**иитемпропертибаг \** _</span><span class="sxs-lookup"><span data-stu-id="cec49-113">Type: \**IItemPropertyBag\** _</span></span>

<span data-ttu-id="cec49-114">Указатель на объект [_ *иитемпропертибаг* \*](iitempropertybag.md) , содержащий сведения об элементе поиска, включая свойства элемента.</span><span class="sxs-lookup"><span data-stu-id="cec49-114">Pointer to an [_ *IItemPropertyBag*\*](iitempropertybag.md) object that contains information about the search item, including the properties of the item.</span></span>

</dd> <dt>

<span data-ttu-id="cec49-115">*ппсеарчитем* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="cec49-115">*ppSearchItem* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="cec49-116">Тип: **[ **исеарчитем**](-search-isearchitem.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="cec49-116">Type: **[**ISearchItem**](-search-isearchitem.md)\*\***</span></span>

<span data-ttu-id="cec49-117">Получает адрес указателя на объект [**исеарчитем**](-search-isearchitem.md) , созданный этим методом.</span><span class="sxs-lookup"><span data-stu-id="cec49-117">Receives the address of a pointer to the [**ISearchItem**](-search-isearchitem.md) object created by this method.</span></span> <span data-ttu-id="cec49-118">Этот объект содержит сведения об элементе поиска, например имя файла элемента.</span><span class="sxs-lookup"><span data-stu-id="cec49-118">This object contains information about the search item, such as the item's file name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cec49-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cec49-119">Return value</span></span>

<span data-ttu-id="cec49-120">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="cec49-120">Type: **HRESULT**</span></span>

<span data-ttu-id="cec49-121">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="cec49-121">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cec49-122">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cec49-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="cec49-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cec49-123">Remarks</span></span>

<span data-ttu-id="cec49-124">Метод **исеарчпротоколуи:: жетсеарчитемфорурл** поддерживается только в Windows XP и windows Server 2003 и больше не должен использоваться.</span><span class="sxs-lookup"><span data-stu-id="cec49-124">The **ISearchProtocolUI::GetSearchItemForUrl** method is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="cec49-125">Для предварительного просмотра вложений с помощью обработчика протоколов стороннего производителя на компьютерах под управлением Windows XP или Windows Server 2003 может потребоваться использовать интерфейс [**исеарчпротоколуи**](-search-isearchprotocolui.md) и следующие API: интерфейсы [**иитемпревиеверекст**](-search-iitempreviewerext.md), [**Иитемпропертибаг**](iitempropertybag.md) и [**исеарчитем**](-search-isearchitem.md) , структура [**линкинфо**](-search-linkinfo.md) и [**перечисление**](-search-linktype.md) типов ссылок.</span><span class="sxs-lookup"><span data-stu-id="cec49-125">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the [**ISearchProtocolUI**](-search-isearchprotocolui.md) interface, and the following APIs: the [**IItemPreviewerExt**](-search-iitempreviewerext.md), [**IItemPropertyBag**](iitempropertybag.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) structure, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="cec49-126">Требования</span><span class="sxs-lookup"><span data-stu-id="cec49-126">Requirements</span></span>



| <span data-ttu-id="cec49-127">Требование</span><span class="sxs-lookup"><span data-stu-id="cec49-127">Requirement</span></span> | <span data-ttu-id="cec49-128">Значение</span><span class="sxs-lookup"><span data-stu-id="cec49-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cec49-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cec49-129">Minimum supported client</span></span><br/> | <span data-ttu-id="cec49-130">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="cec49-130">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="cec49-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cec49-131">Minimum supported server</span></span><br/> | <span data-ttu-id="cec49-132">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cec49-132">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="cec49-133">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="cec49-133">Redistributable</span></span><br/>          | <span data-ttu-id="cec49-134">Поиск на рабочем столе Windows (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="cec49-134">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="cec49-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cec49-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cec49-136">**исеарчпротоколуи**</span><span class="sxs-lookup"><span data-stu-id="cec49-136">**ISearchProtocolUI**</span></span>](-search-isearchprotocolui.md)
</dt> </dl>

 

 




