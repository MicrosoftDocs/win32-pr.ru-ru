---
description: Возвращает объект Исеарчитем, если URL-адрес представляет фактический источник данных оболочки (также известный как расширение пространства имен оболочки).
ms.assetid: 7da6344d-b433-48c3-8f75-7bef0295b9ea
title: 'Метод Исеарчитем:: Жетпарентфолдер'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchItem.GetParentFolder
api_type:
- COM
api_location: ''
ms.openlocfilehash: 4209b319e066d5481c669bcca021684f87532a3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701398"
---
# <a name="isearchitemgetparentfolder-method"></a><span data-ttu-id="1eb8b-103">Метод Исеарчитем:: Жетпарентфолдер</span><span class="sxs-lookup"><span data-stu-id="1eb8b-103">ISearchItem::GetParentFolder method</span></span>

<span data-ttu-id="1eb8b-104">Возвращает объект [**исеарчитем**](-search-isearchitem.md) , если URL-адрес представляет фактический источник данных оболочки (также известный как расширение пространства имен оболочки).</span><span class="sxs-lookup"><span data-stu-id="1eb8b-104">Gets the [**ISearchItem**](-search-isearchitem.md) object if the URL represents an actual Shell data source (also known as a Shell namespace extension).</span></span>

## <a name="syntax"></a><span data-ttu-id="1eb8b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1eb8b-105">Syntax</span></span>


```C++
HRESULT GetParentFolder(
  [out] ppShellFolder **IShellFolder,
  [out] ppidl         *LPITEMIDLIST
);
```



## <a name="parameters"></a><span data-ttu-id="1eb8b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1eb8b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1eb8b-107">*Ишеллфолдер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="1eb8b-107">*IShellFolder* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1eb8b-108">Тип: **ппшеллфолдер \* \***</span><span class="sxs-lookup"><span data-stu-id="1eb8b-108">Type: **ppShellFolder\*\***</span></span>

<span data-ttu-id="1eb8b-109">При возврате содержит адрес указателя на папку, содержащую текущий URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="1eb8b-109">On return, contains the address of a pointer to the folder that contains the current URL.</span></span> <span data-ttu-id="1eb8b-110">[Интерфейс ишеллфолдер](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) предоставляется всеми объектами папки пространства имен оболочки, и его методы используются для управления папками.</span><span class="sxs-lookup"><span data-stu-id="1eb8b-110">[IShellFolder Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) is exposed by all Shell namespace folder objects, and its methods are used to manage folders.</span></span>

</dd> <dt>

<span data-ttu-id="1eb8b-111">*Лпитемидлист* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="1eb8b-111">*LPITEMIDLIST* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1eb8b-112">Тип: \**ппидл \** _</span><span class="sxs-lookup"><span data-stu-id="1eb8b-112">Type: \**ppidl\** _</span></span>

<span data-ttu-id="1eb8b-113">При возврате содержит адрес указателя на список идентификаторов элементов (ПИДЛ), определяющий родительскую папку.</span><span class="sxs-lookup"><span data-stu-id="1eb8b-113">On return, contains the address of a pointer to an item identifier list (PIDL) that identifies the parent folder.</span></span> <span data-ttu-id="1eb8b-114">Параметр _LPITEMIDLIST \* может ссылаться на объект на любом уровне ниже родительской папки в иерархии пространства имен и может быть многоуровневой указателем на **Пидл** относительно родительской папки.</span><span class="sxs-lookup"><span data-stu-id="1eb8b-114">The _LPITEMIDLIST\* parameter can refer to an object at any level below the parent folder in the namespace hierarchy, and can thus be a multi-level pointer to a **pidl** relative to the parent folder.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1eb8b-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1eb8b-115">Return value</span></span>

<span data-ttu-id="1eb8b-116">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="1eb8b-116">Type: **HRESULT**</span></span>

<span data-ttu-id="1eb8b-117">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="1eb8b-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1eb8b-118">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1eb8b-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1eb8b-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1eb8b-119">Remarks</span></span>

<span data-ttu-id="1eb8b-120">Метод **исеарчитем:: жетпарентфолдер** поддерживается только в Windows XP и windows Server 2003 и больше не должен использоваться.</span><span class="sxs-lookup"><span data-stu-id="1eb8b-120">The **ISearchItem::GetParentFolder** method is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="1eb8b-121">Для предварительного просмотра вложений с помощью обработчика протоколов стороннего производителя на компьютерах под управлением Windows XP или Windows Server 2003 может потребоваться использовать интерфейс [**исеарчитем**](-search-isearchitem.md) и следующие API: интерфейсы [**иитемпревиеверекст**](-search-iitempreviewerext.md), [**Иитемпропертибаг**](iitempropertybag.md)и [**исеарчпротоколуи**](-search-isearchprotocolui.md) , структура [**линкинфо**](-search-linkinfo.md) и [**перечисление**](-search-linktype.md) типов ссылок.</span><span class="sxs-lookup"><span data-stu-id="1eb8b-121">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the [**ISearchItem**](-search-isearchitem.md) interface, and the following APIs: the [**IItemPreviewerExt**](-search-iitempreviewerext.md), [**IItemPropertyBag**](iitempropertybag.md), and [**ISearchProtocolUI**](-search-isearchprotocolui.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) structure, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="1eb8b-122">Требования</span><span class="sxs-lookup"><span data-stu-id="1eb8b-122">Requirements</span></span>



| <span data-ttu-id="1eb8b-123">Требование</span><span class="sxs-lookup"><span data-stu-id="1eb8b-123">Requirement</span></span> | <span data-ttu-id="1eb8b-124">Значение</span><span class="sxs-lookup"><span data-stu-id="1eb8b-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1eb8b-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1eb8b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1eb8b-126">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="1eb8b-126">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="1eb8b-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1eb8b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1eb8b-128">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1eb8b-128">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="1eb8b-129">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="1eb8b-129">Redistributable</span></span><br/>          | <span data-ttu-id="1eb8b-130">Поиск на рабочем столе Windows (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="1eb8b-130">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="1eb8b-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1eb8b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1eb8b-132">**исеарчитем**</span><span class="sxs-lookup"><span data-stu-id="1eb8b-132">**ISearchItem**</span></span>](-search-isearchitem.md)
</dt> </dl>

 

 
