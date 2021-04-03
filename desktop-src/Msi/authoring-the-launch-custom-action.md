---
description: Исходный код для примера пользовательского действия с именем Launch, который соответствует примерам спецификаций, предоставляется пакетом SDK установщик Windows в качестве файла Tutorial. cpp.
ms.assetid: 6f6d45b0-759d-4d28-a542-5cdbb589448f
title: Создание настраиваемого действия запуска
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4805b20b2250351927100ad978d8791e7acf045f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998267"
---
# <a name="authoring-the-launch-custom-action"></a><span data-ttu-id="373cd-103">Создание настраиваемого действия запуска</span><span class="sxs-lookup"><span data-stu-id="373cd-103">Authoring the Launch Custom Action</span></span>

<span data-ttu-id="373cd-104">Исходный код для примера пользовательского действия с именем Launch, который соответствует примерам спецификаций, предоставляется пакетом SDK установщик Windows в качестве файла Tutorial. cpp.</span><span class="sxs-lookup"><span data-stu-id="373cd-104">The source code for a sample custom action named Launch, which meets the sample specifications, is provided by the Windows Installer SDK as the file Tutorial.cpp.</span></span> <span data-ttu-id="373cd-105">Это настраиваемое действие использует [**мсиформатрекорд**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) для форматирования строки, содержащей свойства.</span><span class="sxs-lookup"><span data-stu-id="373cd-105">This custom action makes use of [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) to format a string containing properties.</span></span> <span data-ttu-id="373cd-106">Свойство \[ \# филекэй \] разрешается в полный путь к HTML-файлу.</span><span class="sxs-lookup"><span data-stu-id="373cd-106">The property \[\#FileKey\] resolves to the full path of the HTML file.</span></span> <span data-ttu-id="373cd-107">Используйте исходный файл для создания Tutorial.dll файлов.</span><span class="sxs-lookup"><span data-stu-id="373cd-107">Use the source file to create the file Tutorial.dll.</span></span> <span data-ttu-id="373cd-108">Точкой входа для этой библиотеки DLL является Лаунчтуториал.</span><span class="sxs-lookup"><span data-stu-id="373cd-108">The entry point to this DLL is LaunchTutorial.</span></span>

<span data-ttu-id="373cd-109">В примере запуска пользовательского действия вызывается библиотека DLL, написанная на языке C++ и созданная из временного двоичного потока.</span><span class="sxs-lookup"><span data-stu-id="373cd-109">The sample custom action Launch calls a DLL written in C++ and is generated from a temporary binary stream.</span></span> <span data-ttu-id="373cd-110">Настраиваемые действия этого типа включают константы базового типа Мсидбкустомактионтипедлл и Мсидбкустомактионтипебинаридата, которые предоставляют базовый числовой тип, равный 1.</span><span class="sxs-lookup"><span data-stu-id="373cd-110">Custom actions of this type include the base type constants msidbCustomActionTypeDll and msidbCustomActionTypeBinaryData, which give a base numeric type equal to 1.</span></span> <span data-ttu-id="373cd-111">См. раздел [тип настраиваемого действия 1](custom-action-type-1.md).</span><span class="sxs-lookup"><span data-stu-id="373cd-111">See [Custom Action Type 1](custom-action-type-1.md).</span></span> <span data-ttu-id="373cd-112">Так как спецификации должны продолжать установку при сбое настраиваемого действия, запуск также включает в себя необязательную константу **мсидбкустомактионтипеконтинуе**, которая составляет 64.</span><span class="sxs-lookup"><span data-stu-id="373cd-112">Because the specifications require that the installation continue if the custom action fails, Launch also includes the optional constant **msidbCustomActionTypeContinue**, which is 64.</span></span> <span data-ttu-id="373cd-113">См. раздел [Параметры обработки возвращаемых пользовательских действий](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="373cd-113">See [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span> <span data-ttu-id="373cd-114">Общий числовой тип запуска — 65.</span><span class="sxs-lookup"><span data-stu-id="373cd-114">The total numeric type of Launch is 65.</span></span>

<span data-ttu-id="373cd-115">Продолжайте [добавлять запуск в таблицу CustomAction и двоичные таблицы](adding-launch-to-the-customaction-and-binary-tables.md).</span><span class="sxs-lookup"><span data-stu-id="373cd-115">Continue to [Adding Launch to the CustomAction and Binary Tables](adding-launch-to-the-customaction-and-binary-tables.md).</span></span>

 

 



