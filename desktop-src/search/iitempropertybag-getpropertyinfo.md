---
description: Возвращает сведения, необходимые для чтения или сохранения свойств в контейнере свойств. Интерфейс Иитемпропертибаг поддерживается только в Windows XP и Windows Server 2003 и больше не должен использоваться.
ms.assetid: 1667b67d-9dd2-48a6-81dd-c8b06834cef0
title: 'Метод Иитемпропертибаг:: GetPropertyInfo'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPropertyBag.GetPropertyInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: a64b064c6c6d3708edc353db136fcad599d14adb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710903"
---
# <a name="iitempropertybaggetpropertyinfo-method"></a><span data-ttu-id="39dd4-104">Метод Иитемпропертибаг:: GetPropertyInfo</span><span class="sxs-lookup"><span data-stu-id="39dd4-104">IItemPropertyBag::GetPropertyInfo method</span></span>

<span data-ttu-id="39dd4-105">Возвращает сведения, необходимые для чтения или сохранения свойств в контейнере свойств.</span><span class="sxs-lookup"><span data-stu-id="39dd4-105">Gets the information required to read or save the properties in the property bag.</span></span> <span data-ttu-id="39dd4-106">Интерфейс [**иитемпропертибаг**](iitempropertybag.md) поддерживается только в Windows XP и windows Server 2003 и больше не должен использоваться.</span><span class="sxs-lookup"><span data-stu-id="39dd4-106">The [**IItemPropertyBag**](iitempropertybag.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

## <a name="syntax"></a><span data-ttu-id="39dd4-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="39dd4-107">Syntax</span></span>


```C++
HRESULT GetPropertyInfo(
  [in]  ULONG    iProperty,
  [in]  ULONG    cProperties,
  [out] ITEMPROP *pPropBag,
  [out] ULONG    *pcProperties
);
```



## <a name="parameters"></a><span data-ttu-id="39dd4-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="39dd4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39dd4-109">*ипроперти* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="39dd4-109">*iProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39dd4-110">Отсчитываемый от нуля индекс первого свойства, для которого запрашиваются сведения.</span><span class="sxs-lookup"><span data-stu-id="39dd4-110">The zero-based index of the first property for which information is requested.</span></span>

</dd> <dt>

<span data-ttu-id="39dd4-111">*кпропертиес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="39dd4-111">*cProperties* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39dd4-112">Число свойств, для которых необходимо получить сведения.</span><span class="sxs-lookup"><span data-stu-id="39dd4-112">The number of properties to get information for.</span></span> <span data-ttu-id="39dd4-113">Этот аргумент задает количество элементов массива в *ппропбаг*.</span><span class="sxs-lookup"><span data-stu-id="39dd4-113">This argument specifies the number of array elements in *pPropBag*.</span></span>

</dd> <dt>

<span data-ttu-id="39dd4-114">*ппропбаг* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="39dd4-114">*pPropBag* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="39dd4-115">Указатель на массив структур [**итемпроп**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) , которые получают сведения о свойствах.</span><span class="sxs-lookup"><span data-stu-id="39dd4-115">Pointer to an array of [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) structures that receives the information for the properties.</span></span>

</dd> <dt>

<span data-ttu-id="39dd4-116">*пкпропертиес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="39dd4-116">*pcProperties* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="39dd4-117">Получает указатель на переменную **ulong** , которая получает количество свойств, для которых была получена информация.</span><span class="sxs-lookup"><span data-stu-id="39dd4-117">Receives a pointer to a **ULONG** variable that receives the number of properties for which information was retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39dd4-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="39dd4-118">Return value</span></span>

<span data-ttu-id="39dd4-119">Если метод завершается успешно, возвращается значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="39dd4-119">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="39dd4-120">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="39dd4-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="39dd4-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="39dd4-121">Remarks</span></span>

<span data-ttu-id="39dd4-122">Интерфейс [**иитемпропертибаг**](iitempropertybag.md) поддерживается только в Windows XP и windows Server 2003 и больше не должен использоваться.</span><span class="sxs-lookup"><span data-stu-id="39dd4-122">The [**IItemPropertyBag**](iitempropertybag.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="39dd4-123">Для предварительного просмотра вложений с помощью обработчика протоколов стороннего производителя на компьютерах под управлением Windows XP или Windows Server 2003 может потребоваться использовать интерфейс [**иитемпропертибаг**](iitempropertybag.md) и следующие API: интерфейсы [**исеарчпротоколуи**](-search-isearchprotocolui.md), [**Иитемпревиеверекст**](-search-iitempreviewerext.md) и [**исеарчитем**](-search-isearchitem.md) , структуры [**линкинфо**](-search-linkinfo.md) и [**итемпроп**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) и [**перечисление**](-search-linktype.md) типов ссылок.</span><span class="sxs-lookup"><span data-stu-id="39dd4-123">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the [**IItemPropertyBag**](iitempropertybag.md) interface and the following APIs: the [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPreviewerExt**](-search-iitempreviewerext.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) and [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) structures, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="39dd4-124">Требования</span><span class="sxs-lookup"><span data-stu-id="39dd4-124">Requirements</span></span>



| <span data-ttu-id="39dd4-125">Требование</span><span class="sxs-lookup"><span data-stu-id="39dd4-125">Requirement</span></span> | <span data-ttu-id="39dd4-126">Значение</span><span class="sxs-lookup"><span data-stu-id="39dd4-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="39dd4-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="39dd4-127">Minimum supported client</span></span><br/> | <span data-ttu-id="39dd4-128">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="39dd4-128">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="39dd4-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="39dd4-129">Minimum supported server</span></span><br/> | <span data-ttu-id="39dd4-130">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="39dd4-130">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="39dd4-131">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="39dd4-131">Redistributable</span></span><br/>          | <span data-ttu-id="39dd4-132">Поиск на рабочем столе Windows (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="39dd4-132">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="39dd4-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="39dd4-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39dd4-134">**иитемпропертибаг**</span><span class="sxs-lookup"><span data-stu-id="39dd4-134">**IItemPropertyBag**</span></span>](iitempropertybag.md)
</dt> </dl>

 

 




