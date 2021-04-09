---
title: Файлы JScript
description: Файлы JScript
ms.assetid: 5b862e52-5d49-44b4-811c-3dbca5552167
keywords:
- Обложки проигрывателя Windows Media, файлы JScript
- обложки, файлы JScript
- файлы для обложек, JScript
- Файлы JScript для обложки, о
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9123ade6b715ee5302925030545140329c06770c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888943"
---
# <a name="jscript-files"></a><span data-ttu-id="73db8-107">Файлы JScript</span><span class="sxs-lookup"><span data-stu-id="73db8-107">JScript Files</span></span>

<span data-ttu-id="73db8-108">Файлы JScript загружаются с атрибутом **scriptFile** элемента **View** .</span><span class="sxs-lookup"><span data-stu-id="73db8-108">JScript files are loaded with the **scriptFile** attribute of the **VIEW** element.</span></span> <span data-ttu-id="73db8-109">Они должны быть текстовыми файлами и должны использовать расширение имени файла. js.</span><span class="sxs-lookup"><span data-stu-id="73db8-109">They must be text files and should use the file name extension .js.</span></span> <span data-ttu-id="73db8-110">Если у вас есть файл JScript, имя которого совпадает с именем файла определения обложки, то файл JScript будет загружаться одновременно с файлом определения обложки.</span><span class="sxs-lookup"><span data-stu-id="73db8-110">If you have a JScript file that has the same name as the skin definition file, the JScript file will be loaded at the same time as the skin definition file.</span></span> <span data-ttu-id="73db8-111">Например, если имеется файл определения обложки с именем Лауре. WMS и имеется файл JScript с именем laure.js, laure.js файл будет загружен автоматически.</span><span class="sxs-lookup"><span data-stu-id="73db8-111">For example, if you have a skin definition file named laure.wms, and you have a JScript file called laure.js, the laure.js file will be loaded automatically.</span></span>

<span data-ttu-id="73db8-112">Вы можете использовать JScript для создания сложных функциональных возможностей в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="73db8-112">You can use JScript to create elaborate functionality behind your skin.</span></span> <span data-ttu-id="73db8-113">Создавая функции в JScript, вы можете сделать то же самое, что и обложки.</span><span class="sxs-lookup"><span data-stu-id="73db8-113">By creating functions in JScript, you can do almost anything imaginable with skins.</span></span> <span data-ttu-id="73db8-114">Например, можно использовать другой список воспроизведения для каждого дня недели, но в пятницу он всегда имеет один и тот же.</span><span class="sxs-lookup"><span data-stu-id="73db8-114">For example, you could use a different playlist for every day of the week, but always have the same one on Friday.</span></span>

<span data-ttu-id="73db8-115">Дополнительные сведения об использовании JScript с обложками см. [в разделе Использование JScript](using-jscript.md) .</span><span class="sxs-lookup"><span data-stu-id="73db8-115">See [Using JScript](using-jscript.md) for more information about using JScript with skins.</span></span> <span data-ttu-id="73db8-116">Обратите внимание, что Visual Basic Scripting Edition (VBScript), который можно использовать при внедрении элемента управления проигрывателя Windows Media в веб-страницу, не поддерживается для использования с обложками.</span><span class="sxs-lookup"><span data-stu-id="73db8-116">Note that Visual Basic Scripting Edition (VBScript), which can be used when embedding the Windows Media Player control in a webpage, is not supported for use with skins.</span></span>

## <a name="related-topics"></a><span data-ttu-id="73db8-117">См. также</span><span class="sxs-lookup"><span data-stu-id="73db8-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73db8-118">**Файлы обложки**</span><span class="sxs-lookup"><span data-stu-id="73db8-118">**Skin Files**</span></span>](skin-files.md)
</dt> </dl>

 

 




