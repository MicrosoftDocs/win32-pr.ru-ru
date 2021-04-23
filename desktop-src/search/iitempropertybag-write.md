---
description: Вызывает сохранение одного или нескольких свойств в контейнере свойств. Интерфейс Иитемпропертибаг поддерживается только в Windows XP и Windows Server 2003 и больше не должен использоваться.
ms.assetid: 35491fbc-fb1c-4bad-86e8-9f19856ed7cb
title: 'Метод Иитемпропертибаг:: Write'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPropertyBag.Write
api_type:
- COM
api_location: ''
ms.openlocfilehash: 7df66487bba0c2bbef40cf3642754dff56f65835
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144038"
---
# <a name="iitempropertybagwrite-method"></a><span data-ttu-id="59e40-104">Метод Иитемпропертибаг:: Write</span><span class="sxs-lookup"><span data-stu-id="59e40-104">IItemPropertyBag::Write method</span></span>

<span data-ttu-id="59e40-105">Вызывает сохранение одного или нескольких свойств в контейнере свойств.</span><span class="sxs-lookup"><span data-stu-id="59e40-105">Causes one or more properties to be saved into the property bag.</span></span> <span data-ttu-id="59e40-106">Интерфейс [**иитемпропертибаг**](iitempropertybag.md) поддерживается только в Windows XP и windows Server 2003 и больше не должен использоваться.</span><span class="sxs-lookup"><span data-stu-id="59e40-106">The [**IItemPropertyBag**](iitempropertybag.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

## <a name="syntax"></a><span data-ttu-id="59e40-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="59e40-107">Syntax</span></span>


```C++
HRESULT Write(
  [in] ULONG    cProperties,
  [in] ITEMPROP *pPropBag,
  [in] VARIANT  *pvarValue
);
```



## <a name="parameters"></a><span data-ttu-id="59e40-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="59e40-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59e40-109">*кпропертиес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="59e40-109">*cProperties* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59e40-110">Число свойств для сохранения.</span><span class="sxs-lookup"><span data-stu-id="59e40-110">The number of properties to save.</span></span> <span data-ttu-id="59e40-111">Этот аргумент задает количество элементов в массивах по адресу *ппропбаг* и *сервер*.</span><span class="sxs-lookup"><span data-stu-id="59e40-111">This argument specifies the number of elements in the arrays at *pPropBag* and *pvarValue*.</span></span>

</dd> <dt>

<span data-ttu-id="59e40-112">*ппропбаг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="59e40-112">*pPropBag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59e40-113">Указатель на массив структур [**итемпроп**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) , указывающий свойства, которые необходимо сохранить.</span><span class="sxs-lookup"><span data-stu-id="59e40-113">Pointer to an array of [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) structures that specifies the properties to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="59e40-114">*сервер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="59e40-114">*pvarValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59e40-115">Указатель на **вариант** , тип которого зависит от типа данных содержащихся в нем сведений о свойствах.</span><span class="sxs-lookup"><span data-stu-id="59e40-115">Pointer to a **VARIANT** whose type depends on the data type of the property information that it contains.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59e40-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="59e40-116">Return value</span></span>

<span data-ttu-id="59e40-117">Если метод завершается успешно, возвращается значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="59e40-117">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="59e40-118">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="59e40-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="59e40-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="59e40-119">Remarks</span></span>

<span data-ttu-id="59e40-120">Интерфейс [**иитемпропертибаг**](iitempropertybag.md) поддерживается только в Windows XP и windows Server 2003 и больше не должен использоваться.</span><span class="sxs-lookup"><span data-stu-id="59e40-120">The [**IItemPropertyBag**](iitempropertybag.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="59e40-121">Для предварительного просмотра вложений с помощью обработчика протоколов стороннего производителя на компьютерах под управлением Windows XP или Windows Server 2003 может потребоваться использовать интерфейс [**иитемпропертибаг**](iitempropertybag.md) и следующие API: интерфейсы [**исеарчпротоколуи**](-search-isearchprotocolui.md), [**Иитемпревиеверекст**](-search-iitempreviewerext.md) и [**исеарчитем**](-search-isearchitem.md) , структуры [**линкинфо**](-search-linkinfo.md) и [**итемпроп**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) и [**перечисление**](-search-linktype.md) типов ссылок.</span><span class="sxs-lookup"><span data-stu-id="59e40-121">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the [**IItemPropertyBag**](iitempropertybag.md) interface and the following APIs: the [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPreviewerExt**](-search-iitempreviewerext.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) and [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) structures, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="59e40-122">Требования</span><span class="sxs-lookup"><span data-stu-id="59e40-122">Requirements</span></span>



| <span data-ttu-id="59e40-123">Требование</span><span class="sxs-lookup"><span data-stu-id="59e40-123">Requirement</span></span> | <span data-ttu-id="59e40-124">Значение</span><span class="sxs-lookup"><span data-stu-id="59e40-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="59e40-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="59e40-125">Minimum supported client</span></span><br/> | <span data-ttu-id="59e40-126">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="59e40-126">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="59e40-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="59e40-127">Minimum supported server</span></span><br/> | <span data-ttu-id="59e40-128">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="59e40-128">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="59e40-129">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="59e40-129">Redistributable</span></span><br/>          | <span data-ttu-id="59e40-130">Поиск на рабочем столе Windows (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="59e40-130">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="59e40-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="59e40-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59e40-132">**иитемпропертибаг**</span><span class="sxs-lookup"><span data-stu-id="59e40-132">**IItemPropertyBag**</span></span>](iitempropertybag.md)
</dt> </dl>

 

 




