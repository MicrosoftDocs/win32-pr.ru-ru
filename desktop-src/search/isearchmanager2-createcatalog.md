---
description: Создает новый пользовательский каталог в индексаторе поиска Windows и возвращает ссылку на него.
ms.assetid: 2ADC48B8-87A2-4527-9AA8-9B0BA3A12462
title: 'Метод ISearchManager2:: CreateCatalog'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchManager2.CreateCatalog
api_type:
- COM
api_location:
- searchapi.h
ms.openlocfilehash: 009e34a2d1eb4d18df1747ba01ea39c3360ec81a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262929"
---
# <a name="isearchmanager2createcatalog-method"></a><span data-ttu-id="ff63d-103">Метод ISearchManager2:: CreateCatalog</span><span class="sxs-lookup"><span data-stu-id="ff63d-103">ISearchManager2::CreateCatalog method</span></span>

<span data-ttu-id="ff63d-104">Создает новый пользовательский каталог в индексаторе поиска Windows и возвращает ссылку на него.</span><span class="sxs-lookup"><span data-stu-id="ff63d-104">Creates a new custom catalog in the Windows Search indexer and returns a reference to it.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff63d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ff63d-105">Syntax</span></span>


```C++
HRESULT CreateCatalog(
  [in]  LPCWSTR               pszCatalog,
  [out] ISearchCatalogManager **ppCatalogManager
);
```



## <a name="parameters"></a><span data-ttu-id="ff63d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ff63d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff63d-107">*псзкаталог* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ff63d-107">*pszCatalog* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff63d-108">Тип: **[ **лпквстр**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ff63d-108">Type: **[**LPCWSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ff63d-109">Имя создаваемого каталога.</span><span class="sxs-lookup"><span data-stu-id="ff63d-109">Name of catalog to create.</span></span> <span data-ttu-id="ff63d-110">Может быть любым именем, выбранным вызывающим объектом, должно содержать только стандартные алфавитно-цифровые символы и символ подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="ff63d-110">Can be any name selected by the caller, must contain only standard alphanumeric characters and underscore.</span></span>

</dd> <dt>

<span data-ttu-id="ff63d-111">*ппкаталогманажер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ff63d-111">*ppCatalogManager* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ff63d-112">Тип: **[ **исеарчкаталогманажер**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)\*\***</span><span class="sxs-lookup"><span data-stu-id="ff63d-112">Type: **[**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)\*\***</span></span>

<span data-ttu-id="ff63d-113">При успешном выполнении ссылка на созданный каталог возвращается в виде указателя интерфейса [**исеарчкаталогманажер**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) .</span><span class="sxs-lookup"><span data-stu-id="ff63d-113">On success a reference to the created catalog is returned as an [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) interface pointer.</span></span> <span data-ttu-id="ff63d-114">Необходимо вызвать выпуск () для этого интерфейса после того, как вызывающее приложение завершит его использование.</span><span class="sxs-lookup"><span data-stu-id="ff63d-114">The Release() must be called on this interface after the calling application has finished using it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff63d-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ff63d-115">Return value</span></span>

<span data-ttu-id="ff63d-116">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ff63d-116">Type: **HRESULT**</span></span>

<span data-ttu-id="ff63d-117">HRESULT, указывающий состояние операции:</span><span class="sxs-lookup"><span data-stu-id="ff63d-117">HRESULT indicating status of operation:</span></span>



| <span data-ttu-id="ff63d-118">Код возврата</span><span class="sxs-lookup"><span data-stu-id="ff63d-118">Return code</span></span>                                                                             | <span data-ttu-id="ff63d-119">Описание</span><span class="sxs-lookup"><span data-stu-id="ff63d-119">Description</span></span>                                                                                 |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ff63d-120"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="ff63d-120"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="ff63d-121">Каталог ранее не существовал и был создан.</span><span class="sxs-lookup"><span data-stu-id="ff63d-121">Catalog did not previously exist and was created.</span></span> <span data-ttu-id="ff63d-122">Ссылка на возвращенный каталог.</span><span class="sxs-lookup"><span data-stu-id="ff63d-122">Reference to catalog returned.</span></span><br/> |
| <dl> <span data-ttu-id="ff63d-123"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="ff63d-123"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="ff63d-124">Каталог, который существовал ранее, ссылается на возвращенный каталог.</span><span class="sxs-lookup"><span data-stu-id="ff63d-124">Catalog previously existed, reference to catalog returned.</span></span><br/>                       |



 

<span data-ttu-id="ff63d-125">Сбой HRESULT: не удалось создать каталог или переданы недопустимые аргументы.</span><span class="sxs-lookup"><span data-stu-id="ff63d-125">FAILED HRESULT: Failure creating catalog or invalid arguments passed.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff63d-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ff63d-126">Remarks</span></span>

<span data-ttu-id="ff63d-127">Вызывается для создания нового каталога в индексаторе поиска Windows.</span><span class="sxs-lookup"><span data-stu-id="ff63d-127">Called to create a new catalog in the Windows Search indexer.</span></span> <span data-ttu-id="ff63d-128">После создания можно использовать методы возвращенного [**исеарчкаталог**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) Manager для добавления индексируемых расположений, отслеживания процесса индексирования и создания запросов для отправки в индексатор и получения результатов.</span><span class="sxs-lookup"><span data-stu-id="ff63d-128">After creation, the methods on the returned [**ISearchCatalog**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) manager can be used to add locations to be indexed, monitor indexing process, and construct queries to send to the indexer and get results.</span></span> <span data-ttu-id="ff63d-129">Дополнительные сведения см. в документации по управлению индексом. https://msdn.microsoft.com/library/bb266516(VS.85).aspx</span><span class="sxs-lookup"><span data-stu-id="ff63d-129">See the “Managing the Index” documentation for more info: https://msdn.microsoft.com/library/bb266516(VS.85).aspx</span></span>

## <a name="requirements"></a><span data-ttu-id="ff63d-130">Требования</span><span class="sxs-lookup"><span data-stu-id="ff63d-130">Requirements</span></span>



| <span data-ttu-id="ff63d-131">Требование</span><span class="sxs-lookup"><span data-stu-id="ff63d-131">Requirement</span></span> | <span data-ttu-id="ff63d-132">Значение</span><span class="sxs-lookup"><span data-stu-id="ff63d-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ff63d-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ff63d-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ff63d-134">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ff63d-134">Windows 8 \[desktop apps only\]</span></span><br/>           |
| <span data-ttu-id="ff63d-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ff63d-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ff63d-136">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ff63d-136">Windows Server 2012 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ff63d-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ff63d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff63d-138">**ISearchManager2**</span><span class="sxs-lookup"><span data-stu-id="ff63d-138">**ISearchManager2**</span></span>](/windows/desktop/api/searchapi/nn-searchapi-isearchmanager2)
</dt> </dl>

 

 
