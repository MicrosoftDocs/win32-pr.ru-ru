---
description: Допускает расширение к расширенному содержимому для свойства.
ms.assetid: d1b09ea0-7263-4b7c-8c59-25251bb6b285
title: 'Метод Иитемпревиеверекст:: Жетлинкедконтент'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt.GetLinkedContent
api_type:
- COM
api_location: ''
ms.openlocfilehash: 7d450bbda2ac7c24b49d1ca5032fd1c59754652e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719312"
---
# <a name="iitempreviewerextgetlinkedcontent-method"></a><span data-ttu-id="e05a8-103">Метод Иитемпревиеверекст:: Жетлинкедконтент</span><span class="sxs-lookup"><span data-stu-id="e05a8-103">IItemPreviewerExt::GetLinkedContent method</span></span>

<span data-ttu-id="e05a8-104">Допускает расширение к расширенному содержимому для свойства.</span><span class="sxs-lookup"><span data-stu-id="e05a8-104">Permits the extension to rich content for a property.</span></span>

## <a name="syntax"></a><span data-ttu-id="e05a8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e05a8-105">Syntax</span></span>


```C++
HRESULT GetLinkedContent(
  [in]          DWORD     dwContext,
  [in]          LPCOLESTR pwszProp,
  [out, retval] LINKINFO  *pInfo
);
```



## <a name="parameters"></a><span data-ttu-id="e05a8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e05a8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e05a8-107">*двконтекст* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e05a8-107">*dwContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e05a8-108">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="e05a8-108">Type: **DWORD**</span></span>

<span data-ttu-id="e05a8-109">Идентификатор контекста для операции.</span><span class="sxs-lookup"><span data-stu-id="e05a8-109">The context identifier for the operation.</span></span> <span data-ttu-id="e05a8-110">Переопределите *двконтекст* по умолчанию, чтобы задать для идентификатора контекста значение, выбранное вами.</span><span class="sxs-lookup"><span data-stu-id="e05a8-110">Override the *dwContext* default to set the context identifier to a value of your choosing.</span></span>

</dd> <dt>

<span data-ttu-id="e05a8-111">*пвсзпроп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e05a8-111">*pwszProp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e05a8-112">Тип: **лпколестр**</span><span class="sxs-lookup"><span data-stu-id="e05a8-112">Type: **LPCOLESTR**</span></span>

<span data-ttu-id="e05a8-113">Указатель на свойство связанного содержимого в виде строки в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="e05a8-113">A pointer to the property of the linked content as a Unicode string.</span></span>

</dd> <dt>

<span data-ttu-id="e05a8-114">*пинфо* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="e05a8-114">*pInfo* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="e05a8-115">Тип: \**[**линкинфо**](-search-linkinfo.md) \** _</span><span class="sxs-lookup"><span data-stu-id="e05a8-115">Type: \**[**LINKINFO**](-search-linkinfo.md)\** _</span></span>

<span data-ttu-id="e05a8-116">Получает указатель на структуру [_ *линкинфо* \*](-search-linkinfo.md) , в которой метод возвращает сведения о транзакции.</span><span class="sxs-lookup"><span data-stu-id="e05a8-116">Receives a pointer to the [_ *LINKINFO*\*](-search-linkinfo.md) structure in which the method returns information about the transaction.</span></span> <span data-ttu-id="e05a8-117">*пинфо* не должен быть **пустым** указателем.</span><span class="sxs-lookup"><span data-stu-id="e05a8-117">*pInfo* must not be a **NULL** pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e05a8-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e05a8-118">Return value</span></span>

<span data-ttu-id="e05a8-119">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e05a8-119">Type: **HRESULT**</span></span>

<span data-ttu-id="e05a8-120">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="e05a8-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e05a8-121">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e05a8-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e05a8-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e05a8-122">Remarks</span></span>

<span data-ttu-id="e05a8-123">Интерфейс [**иитемпревиеверекст**](-search-iitempreviewerext.md) поддерживается только в Windows XP и windows Server 2003 и больше не должен использоваться.</span><span class="sxs-lookup"><span data-stu-id="e05a8-123">The [**IItemPreviewerExt**](-search-iitempreviewerext.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="e05a8-124">Для предварительного просмотра вложений с помощью обработчика протоколов стороннего производителя на компьютерах под управлением Windows XP или Windows Server 2003 может потребоваться использовать интерфейс [**иитемпревиеверекст**](-search-iitempreviewerext.md) и следующие API: интерфейсы [**исеарчпротоколуи**](-search-isearchprotocolui.md), [**Иитемпропертибаг**](iitempropertybag.md) и [**исеарчитем**](-search-isearchitem.md) , структура [**линкинфо**](-search-linkinfo.md) и [**перечисление**](-search-linktype.md) типов ссылок.</span><span class="sxs-lookup"><span data-stu-id="e05a8-124">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the [**IItemPreviewerExt**](-search-iitempreviewerext.md) interface, and the following APIs: the [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) structure, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="e05a8-125">Требования</span><span class="sxs-lookup"><span data-stu-id="e05a8-125">Requirements</span></span>



| <span data-ttu-id="e05a8-126">Требование</span><span class="sxs-lookup"><span data-stu-id="e05a8-126">Requirement</span></span> | <span data-ttu-id="e05a8-127">Значение</span><span class="sxs-lookup"><span data-stu-id="e05a8-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e05a8-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e05a8-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e05a8-129">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e05a8-129">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="e05a8-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e05a8-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e05a8-131">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e05a8-131">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="e05a8-132">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="e05a8-132">Redistributable</span></span><br/>          | <span data-ttu-id="e05a8-133">Поиск на рабочем столе Windows (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="e05a8-133">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="e05a8-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e05a8-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e05a8-135">**иитемпревиеверекст**</span><span class="sxs-lookup"><span data-stu-id="e05a8-135">**IItemPreviewerExt**</span></span>](-search-iitempreviewerext.md)
</dt> </dl>

 

 




