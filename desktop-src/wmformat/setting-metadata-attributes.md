---
title: Задание атрибутов метаданных
description: Задание атрибутов метаданных
ms.assetid: a5d99361-9919-4548-a24d-900ac65cc634
keywords:
- Windows Media Format SDK, задание атрибутов метаданных
- Расширенный системный формат (ASF), установка атрибутов метаданных
- ASF (Расширенный системный формат), установка атрибутов метаданных
- метаданные, задание атрибутов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfde27d7bc965076d1a4b5f9674c6d198ce61da5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104412553"
---
# <a name="setting-metadata-attributes"></a><span data-ttu-id="5ac8d-107">Задание атрибутов метаданных</span><span class="sxs-lookup"><span data-stu-id="5ac8d-107">Setting Metadata Attributes</span></span>

<span data-ttu-id="5ac8d-108">Атрибуты метаданных задаются с помощью метода [**IWMHeaderInfo3:: аддаттрибуте**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) .</span><span class="sxs-lookup"><span data-stu-id="5ac8d-108">Metadata attributes are set by using the [**IWMHeaderInfo3::AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) method.</span></span>

<span data-ttu-id="5ac8d-109">Всем атрибутам назначается язык из списка языков для файла.</span><span class="sxs-lookup"><span data-stu-id="5ac8d-109">All attributes are assigned a language from the language list for the file.</span></span> <span data-ttu-id="5ac8d-110">Доступ к списку языков можно получить с помощью интерфейса [**ивмлангуажелист**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) .</span><span class="sxs-lookup"><span data-stu-id="5ac8d-110">You can access the language list by using the [**IWMLanguageList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) interface.</span></span> <span data-ttu-id="5ac8d-111">Чтобы получить указатель на интерфейс **ивмлангуажелист** , вызовите метод **QueryInterface** для любого интерфейса объекта, из которого получен [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3).</span><span class="sxs-lookup"><span data-stu-id="5ac8d-111">To get a pointer to an **IWMLanguageList** interface, call **QueryInterface** on any interface of the object from which you have obtained [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3).</span></span>

<span data-ttu-id="5ac8d-112">Вы можете добавить атрибуты с любым именем.</span><span class="sxs-lookup"><span data-stu-id="5ac8d-112">You can add attributes with any name you like.</span></span> <span data-ttu-id="5ac8d-113">Однако использование имен атрибутов, которые не являются стандартными именами, поддерживаемыми пакетом SDK для формата Windows Media, может усложнить поиск пользователями метаданных.</span><span class="sxs-lookup"><span data-stu-id="5ac8d-113">However, using attribute names that are not standard names supported by the Windows Media Format SDK can make your metadata difficult for users to discover.</span></span> <span data-ttu-id="5ac8d-114">Большинство воспроизводимых мультимедийных приложений будут проверять стандартные значения.</span><span class="sxs-lookup"><span data-stu-id="5ac8d-114">Most media-playing applications will check for standard values.</span></span> <span data-ttu-id="5ac8d-115">Дополнительные сведения см. в разделе [пользовательские метаданные](custom-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="5ac8d-115">For more information, see [Custom Metadata](custom-metadata.md).</span></span>

<span data-ttu-id="5ac8d-116">Нельзя использовать потоковый номер 0xFFFF для глобального добавления атрибута.</span><span class="sxs-lookup"><span data-stu-id="5ac8d-116">You cannot use stream number 0xFFFF to add an attribute globally.</span></span> <span data-ttu-id="5ac8d-117">Каждому атрибуту необходимо назначить конкретный номер потока или поток 0 для атрибутов на уровне файла.</span><span class="sxs-lookup"><span data-stu-id="5ac8d-117">You must assign each attribute to a specific stream number, or stream 0 for file-level attributes.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5ac8d-118">См. также</span><span class="sxs-lookup"><span data-stu-id="5ac8d-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ac8d-119">**Работа с метаданными**</span><span class="sxs-lookup"><span data-stu-id="5ac8d-119">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




