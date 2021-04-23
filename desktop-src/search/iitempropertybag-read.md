---
description: Вызывает считывание одного или нескольких свойств из контейнера свойств. Интерфейс Иитемпропертибаг поддерживается только в Windows XP и Windows Server 2003 и больше не должен использоваться.
ms.assetid: 78a63ef0-1b79-4b07-9121-a6fbd1116c4b
title: 'Метод Иитемпропертибаг:: Read'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPropertyBag.Read
api_type:
- COM
api_location: ''
ms.openlocfilehash: ef7af13dc42239a2823d7e7ca9b8def4748519fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342942"
---
# <a name="iitempropertybagread-method"></a><span data-ttu-id="d3e48-104">Метод Иитемпропертибаг:: Read</span><span class="sxs-lookup"><span data-stu-id="d3e48-104">IItemPropertyBag::Read method</span></span>

<span data-ttu-id="d3e48-105">Вызывает считывание одного или нескольких свойств из контейнера свойств.</span><span class="sxs-lookup"><span data-stu-id="d3e48-105">Causes one or more properties to be read from the property bag.</span></span> <span data-ttu-id="d3e48-106">Интерфейс [**иитемпропертибаг**](iitempropertybag.md) поддерживается только в Windows XP и windows Server 2003 и больше не должен использоваться.</span><span class="sxs-lookup"><span data-stu-id="d3e48-106">The [**IItemPropertyBag**](iitempropertybag.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3e48-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d3e48-107">Syntax</span></span>


```C++
HRESULT Read(
  [in]  ULONG    cProperties,
  [in]  ITEMPROP *pPropBag,
  [out] VARIANT  *pvarValue,
  [out] HRESULT  *phrError
);
```



## <a name="parameters"></a><span data-ttu-id="d3e48-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d3e48-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3e48-109">*кпропертиес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d3e48-109">*cProperties* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3e48-110">Число свойств для чтения.</span><span class="sxs-lookup"><span data-stu-id="d3e48-110">The number of properties to read.</span></span> <span data-ttu-id="d3e48-111">Этот аргумент задает количество элементов в массивах по *ппропбаг*, *сервер* и *фреррор*.</span><span class="sxs-lookup"><span data-stu-id="d3e48-111">This argument specifies the number of elements in the arrays at *pPropBag*, *pvarValue*, and *phrError*.</span></span>

</dd> <dt>

<span data-ttu-id="d3e48-112">*ппропбаг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d3e48-112">*pPropBag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3e48-113">Указатель на массив структур [**итемпроп**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) , указывающих запрашиваемые свойства.</span><span class="sxs-lookup"><span data-stu-id="d3e48-113">Pointer to an array of [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) structures that specifies the properties that are requested.</span></span>

</dd> <dt>

<span data-ttu-id="d3e48-114">*сервер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d3e48-114">*pvarValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d3e48-115">Получает указатель, возвращающий массив **вариативных** структур, которые получают значения свойств.</span><span class="sxs-lookup"><span data-stu-id="d3e48-115">Receives a pointer that returns an array of **VARIANT** structures that receives the property values.</span></span>

</dd> <dt>

<span data-ttu-id="d3e48-116">*фреррор* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d3e48-116">*phrError* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d3e48-117">Указатель на массив значений **HRESULT** , которые получают результат каждого прочитанного свойства.</span><span class="sxs-lookup"><span data-stu-id="d3e48-117">Pointer to an array of **HRESULT** values that receives the result of each property read.</span></span> <span data-ttu-id="d3e48-118">В этом массиве должно быть по крайней мере *кпропертиес* элементов.</span><span class="sxs-lookup"><span data-stu-id="d3e48-118">There must be at least *cProperties* elements in this array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3e48-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d3e48-119">Return value</span></span>

<span data-ttu-id="d3e48-120">Если метод завершается успешно, возвращается значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="d3e48-120">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="d3e48-121">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d3e48-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3e48-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d3e48-122">Remarks</span></span>

<span data-ttu-id="d3e48-123">Интерфейс [**иитемпропертибаг**](iitempropertybag.md) поддерживается только в Windows XP и windows Server 2003 и больше не должен использоваться.</span><span class="sxs-lookup"><span data-stu-id="d3e48-123">The [**IItemPropertyBag**](iitempropertybag.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="d3e48-124">Для предварительного просмотра вложений с помощью обработчика протоколов стороннего производителя на компьютерах под управлением Windows XP или Windows Server 2003 может потребоваться использовать интерфейс [**иитемпропертибаг**](iitempropertybag.md) и следующие API: интерфейсы [**исеарчпротоколуи**](-search-isearchprotocolui.md), [**Иитемпревиеверекст**](-search-iitempreviewerext.md) и [**исеарчитем**](-search-isearchitem.md) , структуры [**линкинфо**](-search-linkinfo.md) и [**итемпроп**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) и [**перечисление**](-search-linktype.md) типов ссылок.</span><span class="sxs-lookup"><span data-stu-id="d3e48-124">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the [**IItemPropertyBag**](iitempropertybag.md) interface and the following APIs: the [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPreviewerExt**](-search-iitempreviewerext.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) and [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) structures, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3e48-125">Требования</span><span class="sxs-lookup"><span data-stu-id="d3e48-125">Requirements</span></span>



| <span data-ttu-id="d3e48-126">Требование</span><span class="sxs-lookup"><span data-stu-id="d3e48-126">Requirement</span></span> | <span data-ttu-id="d3e48-127">Значение</span><span class="sxs-lookup"><span data-stu-id="d3e48-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d3e48-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d3e48-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d3e48-129">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="d3e48-129">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d3e48-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d3e48-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d3e48-131">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d3e48-131">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d3e48-132">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="d3e48-132">Redistributable</span></span><br/>          | <span data-ttu-id="d3e48-133">Поиск на рабочем столе Windows (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="d3e48-133">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="d3e48-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d3e48-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3e48-135">**иитемпропертибаг**</span><span class="sxs-lookup"><span data-stu-id="d3e48-135">**IItemPropertyBag**</span></span>](iitempropertybag.md)
</dt> </dl>

 

 




