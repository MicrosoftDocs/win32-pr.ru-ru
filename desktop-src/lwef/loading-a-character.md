---
title: Загрузка символа
description: Загрузка символа
ms.assetid: 973de75b-b530-40c6-896d-e2ab0755ae2c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3590698040f40f8fbf0964177e12ba6ed253c37d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775914"
---
# <a name="loading-a-character"></a><span data-ttu-id="e6c66-103">Загрузка символа</span><span class="sxs-lookup"><span data-stu-id="e6c66-103">Loading a Character</span></span>

<span data-ttu-id="e6c66-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e6c66-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="e6c66-105">Чтобы анимировать символ, необходимо сначала загрузить символ.</span><span class="sxs-lookup"><span data-stu-id="e6c66-105">To animate a character, you must first load the character.</span></span> <span data-ttu-id="e6c66-106">Используйте метод [**Load**](load-method.md) для загрузки данных символа.</span><span class="sxs-lookup"><span data-stu-id="e6c66-106">Use the [**Load**](load-method.md) method to load the character's data.</span></span> <span data-ttu-id="e6c66-107">Microsoft Agent поддерживает два формата для данных символов и анимации: один структурированный файл и отдельные файлы.</span><span class="sxs-lookup"><span data-stu-id="e6c66-107">Microsoft Agent supports two formats for character and animation data: a single structured file and separate files.</span></span> <span data-ttu-id="e6c66-108">Как правило, используется формат одного файла (. ACS), когда данные хранятся локально.</span><span class="sxs-lookup"><span data-stu-id="e6c66-108">Typically, you use the single file format (.ACS) when the data is stored locally.</span></span> <span data-ttu-id="e6c66-109">Формат нескольких файлов (. ACF,. АКА) лучше подходит, если требуется загружать анимацию по отдельности, например при доступе к анимациям с HTTP-сервера.</span><span class="sxs-lookup"><span data-stu-id="e6c66-109">The multiple file format (.ACF, .ACA) works best when you want to download animations individually, such as when accessing animations from an HTTP server.</span></span>

<span data-ttu-id="e6c66-110">Клиентское приложение может загружать только один экземпляр одного и того же символа.</span><span class="sxs-lookup"><span data-stu-id="e6c66-110">A client application can load only a single instance of the same character.</span></span> <span data-ttu-id="e6c66-111">Любая попытка загрузить один и тот же символ несколько раз завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="e6c66-111">Any attempt to load the same character more than once will fail.</span></span> <span data-ttu-id="e6c66-112">Однако в приложении может быть загружено несколько экземпляров одного и того же символа путем предоставления отдельных подключений к Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="e6c66-112">However, an application can have multiple instances of the same character loaded by providing separate connections to Microsoft Agent.</span></span> <span data-ttu-id="e6c66-113">Например, приложение может загрузить один и тот же символ из двух копий элемента управления Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="e6c66-113">For example, an application could load the same character from two copies of the Microsoft Agent control.</span></span>

<span data-ttu-id="e6c66-114">Можно также определить собственные символы для использования с Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="e6c66-114">You can also define your own characters for use with Microsoft Agent.</span></span> <span data-ttu-id="e6c66-115">Вы можете использовать любое средство визуализации, которое предпочитает создавать изображения, при условии, что вы используете файлы формата точечных рисунков Windows.</span><span class="sxs-lookup"><span data-stu-id="e6c66-115">You may use any rendering tool you prefer to create the images, provided that you end up with Windows bitmap format files.</span></span> <span data-ttu-id="e6c66-116">Чтобы собрать и скомпилировать изображения символов в анимации для использования с Microsoft Agent, используйте редактор символов Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="e6c66-116">To assemble and compile a character's images into animations for use with Microsoft Agent, use the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="e6c66-117">Это средство позволяет определить свойства символа по умолчанию, а также определить анимацию для символа.</span><span class="sxs-lookup"><span data-stu-id="e6c66-117">This tool enables you to define a character's default properties as well as define animations for the character.</span></span> <span data-ttu-id="e6c66-118">Редактор символов Microsoft Agent также позволяет выбрать соответствующий формат файла при создании символа.</span><span class="sxs-lookup"><span data-stu-id="e6c66-118">The Microsoft Agent Character Editor also enables you to select the appropriate file format when you create a character.</span></span>

 

 




