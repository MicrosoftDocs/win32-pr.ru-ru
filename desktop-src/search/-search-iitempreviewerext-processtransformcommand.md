---
description: Разрешает обработку команды преобразования, обнаруженной в шаблоне предварительной версии.
ms.assetid: 0b81b780-8bd1-4667-a0a1-65319f209603
title: 'Иитемпревиеверекст: метод:P Роцесстрансформкомманд'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt.ProcessTransformCommand
api_type:
- COM
api_location: ''
ms.openlocfilehash: 384294aac177679ea7445edb880198d250310625
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896941"
---
# <a name="iitempreviewerextprocesstransformcommand-method"></a><span data-ttu-id="5766b-103">Иитемпревиеверекст: метод:P Роцесстрансформкомманд</span><span class="sxs-lookup"><span data-stu-id="5766b-103">IItemPreviewerExt::ProcessTransformCommand method</span></span>

<span data-ttu-id="5766b-104">Разрешает обработку команды преобразования, обнаруженной в шаблоне предварительной версии.</span><span class="sxs-lookup"><span data-stu-id="5766b-104">Permits processing of a transformation command encountered in a preview template.</span></span>

## <a name="syntax"></a><span data-ttu-id="5766b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5766b-105">Syntax</span></span>


```C++
HRESULT ProcessTransformCommand(
  [in]          DWORD     dwContext,
  [in]          LPCOLESTR pwszName,
  [in]          LPCOLESTR pwszArg,
  [out, retval] VARIANT   *pvarResult
);
```



## <a name="parameters"></a><span data-ttu-id="5766b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5766b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5766b-107">*двконтекст* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5766b-107">*dwContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5766b-108">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="5766b-108">Type: **DWORD**</span></span>

<span data-ttu-id="5766b-109">Идентификатор контекста для операции.</span><span class="sxs-lookup"><span data-stu-id="5766b-109">The context identifier for the operation.</span></span> <span data-ttu-id="5766b-110">Переопределите *двконтекст* по умолчанию, чтобы задать для идентификатора контекста значение, выбранное вами.</span><span class="sxs-lookup"><span data-stu-id="5766b-110">Override the *dwContext* default to set the context identifier to a value of your choosing.</span></span>

</dd> <dt>

<span data-ttu-id="5766b-111">*pwszName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5766b-111">*pwszName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5766b-112">Тип: **лпколестр**</span><span class="sxs-lookup"><span data-stu-id="5766b-112">Type: **LPCOLESTR**</span></span>

<span data-ttu-id="5766b-113">Указатель на имя команды преобразования в виде строки Юникода.</span><span class="sxs-lookup"><span data-stu-id="5766b-113">A pointer to the name of the transformation command as a Unicode string.</span></span>

</dd> <dt>

<span data-ttu-id="5766b-114">*пвсзарг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5766b-114">*pwszArg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5766b-115">Тип: **лпколестр**</span><span class="sxs-lookup"><span data-stu-id="5766b-115">Type: **LPCOLESTR**</span></span>

<span data-ttu-id="5766b-116">Указатель на аргумент в виде строки в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="5766b-116">A pointer to the argument as a Unicode string.</span></span>

</dd> <dt>

<span data-ttu-id="5766b-117">*пварресулт* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="5766b-117">*pvarResult* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="5766b-118">Тип: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="5766b-118">Type: \**VARIANT\** _</span></span>

<span data-ttu-id="5766b-119">Указатель на результирующий вариант.</span><span class="sxs-lookup"><span data-stu-id="5766b-119">A pointer to the result variant.</span></span> <span data-ttu-id="5766b-120">_pvarResult \* не должен быть **пустым** указателем.</span><span class="sxs-lookup"><span data-stu-id="5766b-120">_pvarResult\* must not be a **NULL** pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5766b-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5766b-121">Return value</span></span>

<span data-ttu-id="5766b-122">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="5766b-122">Type: **HRESULT**</span></span>

<span data-ttu-id="5766b-123">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="5766b-123">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5766b-124">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5766b-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5766b-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5766b-125">Remarks</span></span>

<span data-ttu-id="5766b-126">Интерфейс [**иитемпревиеверекст**](-search-iitempreviewerext.md) поддерживается только в Windows XP и windows Server 2003 и больше не должен использоваться.</span><span class="sxs-lookup"><span data-stu-id="5766b-126">The [**IItemPreviewerExt**](-search-iitempreviewerext.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="5766b-127">Для предварительного просмотра вложений с помощью обработчика протоколов стороннего производителя на компьютерах под управлением Windows XP или Windows Server 2003 может потребоваться использовать интерфейс [**иитемпревиеверекст**](-search-iitempreviewerext.md) и следующие API: интерфейсы [**исеарчпротоколуи**](-search-isearchprotocolui.md), [**Иитемпропертибаг**](iitempropertybag.md) и [**исеарчитем**](-search-isearchitem.md) , структура [**линкинфо**](-search-linkinfo.md) и [**перечисление**](-search-linktype.md) типов ссылок.</span><span class="sxs-lookup"><span data-stu-id="5766b-127">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the [**IItemPreviewerExt**](-search-iitempreviewerext.md) interface, and the following APIs: the [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) structure, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="5766b-128">Требования</span><span class="sxs-lookup"><span data-stu-id="5766b-128">Requirements</span></span>



| <span data-ttu-id="5766b-129">Требование</span><span class="sxs-lookup"><span data-stu-id="5766b-129">Requirement</span></span> | <span data-ttu-id="5766b-130">Значение</span><span class="sxs-lookup"><span data-stu-id="5766b-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5766b-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5766b-131">Minimum supported client</span></span><br/> | <span data-ttu-id="5766b-132">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="5766b-132">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="5766b-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5766b-133">Minimum supported server</span></span><br/> | <span data-ttu-id="5766b-134">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5766b-134">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="5766b-135">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="5766b-135">Redistributable</span></span><br/>          | <span data-ttu-id="5766b-136">Поиск на рабочем столе Windows (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="5766b-136">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="5766b-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5766b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5766b-138">**иитемпревиеверекст**</span><span class="sxs-lookup"><span data-stu-id="5766b-138">**IItemPreviewerExt**</span></span>](-search-iitempreviewerext.md)
</dt> </dl>

 

 




