---
description: Интерфейс Имедиалокатор предоставляет методы для проверки имен файлов в службах редактирования DirectShow (DES).
ms.assetid: 6c1ae957-a2be-454b-9451-772e4a670677
title: Интерфейс Имедиалокатор (Кедит. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaLocator
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9664bf793e989c5975bcef0e712a550399c4ddee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674932"
---
# <a name="imedialocator-interface"></a><span data-ttu-id="24c0a-103">Интерфейс Имедиалокатор</span><span class="sxs-lookup"><span data-stu-id="24c0a-103">IMediaLocator interface</span></span>

> [!Note]  
> <span data-ttu-id="24c0a-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="24c0a-104">\[Deprecated.</span></span> <span data-ttu-id="24c0a-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="24c0a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="24c0a-106">`IMediaLocator`Интерфейс предоставляет методы для проверки имен файлов в [службах редактирования DirectShow](directshow-editing-services.md) (DES).</span><span class="sxs-lookup"><span data-stu-id="24c0a-106">The `IMediaLocator` interface provides methods for validating file names in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="24c0a-107">Используйте этот интерфейс, чтобы убедиться, что заданное имя файла и путь соответствуют существующему файлу.</span><span class="sxs-lookup"><span data-stu-id="24c0a-107">Use this interface to ensure that a given file name and path correspond to an existing file.</span></span> <span data-ttu-id="24c0a-108">Этот интерфейс также позволяет искать файл в других местах и отображать **открытое** диалоговое окно, чтобы пользователь мог найти файл.</span><span class="sxs-lookup"><span data-stu-id="24c0a-108">This interface also provides a way to search for the file at other locations, and to display an **Open** dialog box so that the user can locate the file.</span></span>

<span data-ttu-id="24c0a-109">Указатель мультимедиа реализует этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="24c0a-109">The media locator implements this interface.</span></span> <span data-ttu-id="24c0a-110">Временная шкала и модуль визуализации также поддерживают проверку имени файла с помощью следующих методов:</span><span class="sxs-lookup"><span data-stu-id="24c0a-110">The timeline and the render engine also support file name validation through the following methods:</span></span>

-   <span data-ttu-id="24c0a-111">[**Иамтимелине:: валидатесаурценамес**](iamtimeline-validatesourcenames.md): проверяет и обновляет имена файлов на временной шкале.</span><span class="sxs-lookup"><span data-stu-id="24c0a-111">[**IAMTimeline::ValidateSourceNames**](iamtimeline-validatesourcenames.md): Validates and updates file names in the timeline.</span></span>
-   <span data-ttu-id="24c0a-112">[**Ирендеренгине:: сетсаурценамевалидатион**](irenderengine-setsourcenamevalidation.md): указывает, как подсистема подготовки отчетов проверяет имена файлов во время отрисовки.</span><span class="sxs-lookup"><span data-stu-id="24c0a-112">[**IRenderEngine::SetSourceNameValidation**](irenderengine-setsourcenamevalidation.md): Specifies how the render engine validates file names at rendering time.</span></span>

<span data-ttu-id="24c0a-113">Как правило, приложение DES вызывает эти методы, а не создает экземпляр указателя мультимедиа напрямую.</span><span class="sxs-lookup"><span data-stu-id="24c0a-113">Typically, a DES application will call these methods rather than directly create an instance of the media locator.</span></span> <span data-ttu-id="24c0a-114">Дополнительные сведения см. [в разделе Использование указателя мультимедиа](using-the-media-locator.md).</span><span class="sxs-lookup"><span data-stu-id="24c0a-114">For more information, see [Using the Media Locator](using-the-media-locator.md).</span></span>

## <a name="members"></a><span data-ttu-id="24c0a-115">Элементы</span><span class="sxs-lookup"><span data-stu-id="24c0a-115">Members</span></span>

<span data-ttu-id="24c0a-116">Интерфейс **имедиалокатор** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="24c0a-116">The **IMediaLocator** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="24c0a-117">**Имедиалокатор** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="24c0a-117">**IMediaLocator** also has these types of members:</span></span>

-   [<span data-ttu-id="24c0a-118">Методы</span><span class="sxs-lookup"><span data-stu-id="24c0a-118">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="24c0a-119">Методы</span><span class="sxs-lookup"><span data-stu-id="24c0a-119">Methods</span></span>

<span data-ttu-id="24c0a-120">Интерфейс **имедиалокатор** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="24c0a-120">The **IMediaLocator** interface has these methods.</span></span>



| <span data-ttu-id="24c0a-121">Метод</span><span class="sxs-lookup"><span data-stu-id="24c0a-121">Method</span></span>                                                     | <span data-ttu-id="24c0a-122">Описание</span><span class="sxs-lookup"><span data-stu-id="24c0a-122">Description</span></span>                                                                        |
|:-----------------------------------------------------------|:-----------------------------------------------------------------------------------|
| [<span data-ttu-id="24c0a-123">**аддфаундлокатион**</span><span class="sxs-lookup"><span data-stu-id="24c0a-123">**AddFoundLocation**</span></span>](imedialocator-addfoundlocation.md) | <span data-ttu-id="24c0a-124">Добавляет каталог в кэш каталога.</span><span class="sxs-lookup"><span data-stu-id="24c0a-124">Adds a directory to the directory cache.</span></span><br/>                                |
| [<span data-ttu-id="24c0a-125">**финдмедиафиле**</span><span class="sxs-lookup"><span data-stu-id="24c0a-125">**FindMediaFile**</span></span>](imedialocator-findmediafile.md)       | <span data-ttu-id="24c0a-126">Выполняет поиск файла и, при успешном выполнении, извлекает путь к файлу.</span><span class="sxs-lookup"><span data-stu-id="24c0a-126">Searches for a file and, if successful, retrieves the path to the file.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="24c0a-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="24c0a-127">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="24c0a-128">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="24c0a-128">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="24c0a-129">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="24c0a-129">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="24c0a-130">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="24c0a-130">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="24c0a-131">Требования</span><span class="sxs-lookup"><span data-stu-id="24c0a-131">Requirements</span></span>



| <span data-ttu-id="24c0a-132">Требование</span><span class="sxs-lookup"><span data-stu-id="24c0a-132">Requirement</span></span> | <span data-ttu-id="24c0a-133">Значение</span><span class="sxs-lookup"><span data-stu-id="24c0a-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="24c0a-134">Header</span><span class="sxs-lookup"><span data-stu-id="24c0a-134">Header</span></span><br/>  | <dl> <span data-ttu-id="24c0a-135"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="24c0a-135"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="24c0a-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="24c0a-136">Library</span></span><br/> | <dl> <span data-ttu-id="24c0a-137"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="24c0a-137"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
