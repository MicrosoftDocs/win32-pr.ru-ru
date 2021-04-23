---
description: Интерфейс IXml2Dex сохраняет и загружает файлы проекта служб редактирования DirectShow (DES) в язык XML (XML). Этот интерфейс также предоставляет методы для чтения и записи файлов графа DirectShow (. ГРФ).
ms.assetid: a07b0cbe-1f1d-4ccd-a994-9bb1a49c78d8
title: Интерфейс IXml2Dex (Кедит. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ac15110aa1482c37a835ae874057a792e310fc2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689330"
---
# <a name="ixml2dex-interface"></a><span data-ttu-id="50a7f-104">Интерфейс IXml2Dex</span><span class="sxs-lookup"><span data-stu-id="50a7f-104">IXml2Dex interface</span></span>

> [!Note]  
> <span data-ttu-id="50a7f-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="50a7f-105">\[Deprecated.</span></span> <span data-ttu-id="50a7f-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="50a7f-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="50a7f-107">`IXml2Dex`Интерфейс сохраняет и загружает файлы проекта [служб редактирования DirectShow](directshow-editing-services.md) (DES) в язык XML (XML).</span><span class="sxs-lookup"><span data-stu-id="50a7f-107">The `IXml2Dex` interface saves and loads [DirectShow Editing Services](directshow-editing-services.md) (DES) project files in Extensible Markup Language (XML).</span></span> <span data-ttu-id="50a7f-108">Этот интерфейс также предоставляет методы для чтения и записи файлов графа DirectShow (. ГРФ).</span><span class="sxs-lookup"><span data-stu-id="50a7f-108">This interface also provides methods for reading and writing DirectShow graph (.grf) files.</span></span>

## <a name="members"></a><span data-ttu-id="50a7f-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="50a7f-109">Members</span></span>

<span data-ttu-id="50a7f-110">Интерфейс **IXml2Dex** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="50a7f-110">The **IXml2Dex** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="50a7f-111">**IXml2Dex** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="50a7f-111">**IXml2Dex** also has these types of members:</span></span>

-   [<span data-ttu-id="50a7f-112">Методы</span><span class="sxs-lookup"><span data-stu-id="50a7f-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="50a7f-113">Методы</span><span class="sxs-lookup"><span data-stu-id="50a7f-113">Methods</span></span>

<span data-ttu-id="50a7f-114">Интерфейс **IXml2Dex** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="50a7f-114">The **IXml2Dex** interface has these methods.</span></span>



| <span data-ttu-id="50a7f-115">Метод</span><span class="sxs-lookup"><span data-stu-id="50a7f-115">Method</span></span>                                                      | <span data-ttu-id="50a7f-116">Описание</span><span class="sxs-lookup"><span data-stu-id="50a7f-116">Description</span></span>                                                                |
|:------------------------------------------------------------|:---------------------------------------------------------------------------|
| [<span data-ttu-id="50a7f-117">**копиксмл**</span><span class="sxs-lookup"><span data-stu-id="50a7f-117">**CopyXML**</span></span>](ixml2dex-copyxml.md)                         | <span data-ttu-id="50a7f-118">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="50a7f-118">Not implemented.</span></span><br/>                                                |
| [<span data-ttu-id="50a7f-119">**креатеграффромфиле**</span><span class="sxs-lookup"><span data-stu-id="50a7f-119">**CreateGraphFromFile**</span></span>](ixml2dex-creategraphfromfile.md) | <span data-ttu-id="50a7f-120">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="50a7f-120">Not implemented.</span></span><br/>                                                |
| [<span data-ttu-id="50a7f-121">**Удалить**</span><span class="sxs-lookup"><span data-stu-id="50a7f-121">**Delete**</span></span>](ixml2dex-delete.md)                           | <span data-ttu-id="50a7f-122">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="50a7f-122">Not implemented.</span></span><br/>                                                |
| [<span data-ttu-id="50a7f-123">**пастексмл**</span><span class="sxs-lookup"><span data-stu-id="50a7f-123">**PasteXML**</span></span>](ixml2dex-pastexml.md)                       | <span data-ttu-id="50a7f-124">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="50a7f-124">Not implemented.</span></span><br/>                                                |
| [<span data-ttu-id="50a7f-125">**пастексмлфиле**</span><span class="sxs-lookup"><span data-stu-id="50a7f-125">**PasteXMLFile**</span></span>](ixml2dex-pastexmlfile.md)               | <span data-ttu-id="50a7f-126">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="50a7f-126">Not implemented.</span></span><br/>                                                |
| [<span data-ttu-id="50a7f-127">**Метода**</span><span class="sxs-lookup"><span data-stu-id="50a7f-127">**ReadXML**</span></span>](ixml2dex-readxml.md)                         | <span data-ttu-id="50a7f-128">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="50a7f-128">Not implemented.</span></span><br/>                                                |
| [<span data-ttu-id="50a7f-129">**реадксмлфиле**</span><span class="sxs-lookup"><span data-stu-id="50a7f-129">**ReadXMLFile**</span></span>](ixml2dex-readxmlfile.md)                 | <span data-ttu-id="50a7f-130">Загружает файл XML-проекта.</span><span class="sxs-lookup"><span data-stu-id="50a7f-130">Loads an XML project file.</span></span><br/>                                      |
| [<span data-ttu-id="50a7f-131">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="50a7f-131">**Reset**</span></span>](ixml2dex-reset.md)                             | <span data-ttu-id="50a7f-132">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="50a7f-132">Not implemented.</span></span><br/>                                                |
| [<span data-ttu-id="50a7f-133">**вритегрффиле**</span><span class="sxs-lookup"><span data-stu-id="50a7f-133">**WriteGrfFile**</span></span>](ixml2dex-writegrffile.md)               | <span data-ttu-id="50a7f-134">Записывает граф фильтра в файл в формате ГРФ.</span><span class="sxs-lookup"><span data-stu-id="50a7f-134">Writes a filter graph to a file in .grf format.</span></span><br/>                 |
| [<span data-ttu-id="50a7f-135">**WriteXML**</span><span class="sxs-lookup"><span data-stu-id="50a7f-135">**WriteXML**</span></span>](ixml2dex-writexml.md)                       | <span data-ttu-id="50a7f-136">Преобразует временную шкалу в XML-строку.</span><span class="sxs-lookup"><span data-stu-id="50a7f-136">Translates a timeline to an XML string.</span></span><br/>                         |
| [<span data-ttu-id="50a7f-137">**вритексмлфиле**</span><span class="sxs-lookup"><span data-stu-id="50a7f-137">**WriteXMLFile**</span></span>](ixml2dex-writexmlfile.md)               | <span data-ttu-id="50a7f-138">Преобразует временную шкалу в XML и записывает XML-данные в файл.</span><span class="sxs-lookup"><span data-stu-id="50a7f-138">Translates a timeline to XML and writes the XML data to a file.</span></span><br/> |
| [<span data-ttu-id="50a7f-139">**вритексмлпарт**</span><span class="sxs-lookup"><span data-stu-id="50a7f-139">**WriteXMLPart**</span></span>](ixml2dex-writexmlpart.md)               | <span data-ttu-id="50a7f-140">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="50a7f-140">Not implemented.</span></span><br/>                                                |



 

## <a name="remarks"></a><span data-ttu-id="50a7f-141">Комментарии</span><span class="sxs-lookup"><span data-stu-id="50a7f-141">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="50a7f-142">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="50a7f-142">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="50a7f-143">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="50a7f-143">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="50a7f-144">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="50a7f-144">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="50a7f-145">Требования</span><span class="sxs-lookup"><span data-stu-id="50a7f-145">Requirements</span></span>



| <span data-ttu-id="50a7f-146">Требование</span><span class="sxs-lookup"><span data-stu-id="50a7f-146">Requirement</span></span> | <span data-ttu-id="50a7f-147">Значение</span><span class="sxs-lookup"><span data-stu-id="50a7f-147">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="50a7f-148">Версия</span><span class="sxs-lookup"><span data-stu-id="50a7f-148">Version</span></span><br/> | <span data-ttu-id="50a7f-149">Internet Explorer 4,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="50a7f-149">Internet Explorer 4.0 or later</span></span><br/>                                               |
| <span data-ttu-id="50a7f-150">Header</span><span class="sxs-lookup"><span data-stu-id="50a7f-150">Header</span></span><br/>  | <dl> <span data-ttu-id="50a7f-151"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="50a7f-151"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="50a7f-152">Библиотека</span><span class="sxs-lookup"><span data-stu-id="50a7f-152">Library</span></span><br/> | <dl> <span data-ttu-id="50a7f-153"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="50a7f-153"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
