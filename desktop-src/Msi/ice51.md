---
description: ICE51 проверяет, предоставлено ли название для файлов ресурсов шрифтов.
ms.assetid: 5a57ba6e-d1fe-44ab-b72d-52b1f212c322
title: ICE51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38082d754564eead6d60a62e3b4cdcf9b1f0f94f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265832"
---
# <a name="ice51"></a><span data-ttu-id="25124-103">ICE51</span><span class="sxs-lookup"><span data-stu-id="25124-103">ICE51</span></span>

<span data-ttu-id="25124-104">ICE51 проверяет, предоставлено ли название для файлов ресурсов шрифтов.</span><span class="sxs-lookup"><span data-stu-id="25124-104">ICE51 checks that a title has been provided for font resource files.</span></span>

<span data-ttu-id="25124-105">Необходимо указать заголовок для ресурса шрифта, который не имеет внедренного имени.</span><span class="sxs-lookup"><span data-stu-id="25124-105">You must provide a title for a font resource that does not have an embedded name.</span></span> <span data-ttu-id="25124-106">Для файлов ресурсов шрифта. ТТК,. ttf и. ОТФ не требуется заголовок, так как эти файлы содержат внедренное имя.</span><span class="sxs-lookup"><span data-stu-id="25124-106">Only .ttc, .ttf, and .otf font resource files do not require a title, because these files contain an embedded name.</span></span> <span data-ttu-id="25124-107">Не следует указывать заголовок для ресурса шрифта, содержащего внедренное имя, так как система затем регистрирует шрифт дважды.</span><span class="sxs-lookup"><span data-stu-id="25124-107">Do not provide a title for a font resource that contains an embedded name because the system then registers the font twice.</span></span>

<span data-ttu-id="25124-108">**[Установщик Windows 4,5 и более ранних версий](not-supported-in-windows-installer-4-5.md):** ICE51 не проверяет файлы ресурсов шрифтов ОТФ.</span><span class="sxs-lookup"><span data-stu-id="25124-108">**[Windows Installer 4.5 and earlier](not-supported-in-windows-installer-4-5.md):** ICE51 does not check .otf font resource files.</span></span>

## <a name="result"></a><span data-ttu-id="25124-109">Результат</span><span class="sxs-lookup"><span data-stu-id="25124-109">Result</span></span>

<span data-ttu-id="25124-110">ICE51 отправляет сообщение об ошибке, если существуют файлы ресурсов шрифтов. ТТК,. ttf и. ОТФ с заголовками.</span><span class="sxs-lookup"><span data-stu-id="25124-110">ICE51 posts an error if there are any .ttc, .ttf, and .otf font resource files with titles.</span></span> <span data-ttu-id="25124-111">ICE51 отправляет предупреждение, если есть другие файлы ресурсов шрифтов без заголовка.</span><span class="sxs-lookup"><span data-stu-id="25124-111">ICE51 posts a warning if there are any other font resource files without a title.</span></span>

## <a name="example"></a><span data-ttu-id="25124-112">Пример</span><span class="sxs-lookup"><span data-stu-id="25124-112">Example</span></span>

<span data-ttu-id="25124-113">ICE51 сообщит о следующем предупреждении для показанного примера.</span><span class="sxs-lookup"><span data-stu-id="25124-113">ICE51 would report the following warning for the example shown.</span></span>

``` syntax
Font 'Font1' is a TTC\TTF\OTF font, but also has a title.
```

<span data-ttu-id="25124-114">ICE51 выдаст следующее сообщение об ошибке для приведенного примера.</span><span class="sxs-lookup"><span data-stu-id="25124-114">ICE51 would report the following error message for the example shown.</span></span>

``` syntax
Font 'Font2' does not have a title. Only TTC\TTF\OTF fonts do not need titles.
```

<span data-ttu-id="25124-115">[Таблица файлов](file-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="25124-115">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="25124-116">Файл</span><span class="sxs-lookup"><span data-stu-id="25124-116">File</span></span>  | <span data-ttu-id="25124-117">FileName</span><span class="sxs-lookup"><span data-stu-id="25124-117">FileName</span></span>  |
|-------|-----------|
| <span data-ttu-id="25124-118">Font1</span><span class="sxs-lookup"><span data-stu-id="25124-118">Font1</span></span> | <span data-ttu-id="25124-119">font1. ttf</span><span class="sxs-lookup"><span data-stu-id="25124-119">font1.ttf</span></span> |
| <span data-ttu-id="25124-120">Font2</span><span class="sxs-lookup"><span data-stu-id="25124-120">Font2</span></span> | <span data-ttu-id="25124-121">font2. FON</span><span class="sxs-lookup"><span data-stu-id="25124-121">font2.fon</span></span> |



 

[<span data-ttu-id="25124-122">Таблица шрифтов</span><span class="sxs-lookup"><span data-stu-id="25124-122">Font Table</span></span>](font-table.md)



| <span data-ttu-id="25124-123">Файл\_</span><span class="sxs-lookup"><span data-stu-id="25124-123">File\_</span></span> | <span data-ttu-id="25124-124">фонттитле</span><span class="sxs-lookup"><span data-stu-id="25124-124">FontTitle</span></span>          |
|--------|--------------------|
| <span data-ttu-id="25124-125">Font1</span><span class="sxs-lookup"><span data-stu-id="25124-125">Font1</span></span>  | <span data-ttu-id="25124-126">Очень крутой шрифт</span><span class="sxs-lookup"><span data-stu-id="25124-126">A Really Cool Font</span></span> |
| <span data-ttu-id="25124-127">Font2</span><span class="sxs-lookup"><span data-stu-id="25124-127">Font2</span></span>  |                    |



 

## <a name="related-topics"></a><span data-ttu-id="25124-128">См. также</span><span class="sxs-lookup"><span data-stu-id="25124-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="25124-129">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="25124-129">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



