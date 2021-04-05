---
title: О функциях и макросах Авифиле
description: О функциях и макросах Авифиле
ms.assetid: 877f6759-8271-47eb-8a7f-540393e5ae89
keywords:
- Функция Авифилеинит
- Функция Авифиликсит
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f66bbac900b69841fd7cba814aad339731b75727
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068586"
---
# <a name="about-avifile-functions-and-macros"></a><span data-ttu-id="d1528-105">О функциях и макросах Авифиле</span><span class="sxs-lookup"><span data-stu-id="d1528-105">About AVIFile Functions and Macros</span></span>

<span data-ttu-id="d1528-106">Функции и макросы Авифиле обрабатывали информацию в файлах на основе времени как один или несколько *потоков данных* вместо блоков данных, называемых фрагментами.</span><span class="sxs-lookup"><span data-stu-id="d1528-106">The AVIFile functions and macros handle the information in time-based files as one or more *data streams* instead of tagged blocks of data called chunks.</span></span> <span data-ttu-id="d1528-107">Потоки данных ссылаются на компоненты файла на основе времени.</span><span class="sxs-lookup"><span data-stu-id="d1528-107">Data streams refer to the components of a time-based file.</span></span> <span data-ttu-id="d1528-108">Файл AVI может содержать несколько различных типов данных, таких как последовательность видео, звуковая дорожка на английском языке и французская звуковая дорожка.</span><span class="sxs-lookup"><span data-stu-id="d1528-108">An AVI file can contain several different types of data, such as a video sequence, an English soundtrack, and a French soundtrack.</span></span> <span data-ttu-id="d1528-109">С помощью Авифиле приложение может обращаться к каждому из этих компонентов отдельно.</span><span class="sxs-lookup"><span data-stu-id="d1528-109">Using AVIFile, an application can access each of these components separately.</span></span>

> [!Note]  
> <span data-ttu-id="d1528-110">Несмотря на то что функции и макросы Авифиле работают с любым файлом Metallica, в этом обзоре показано, как использовать его только с файлами AVI.</span><span class="sxs-lookup"><span data-stu-id="d1528-110">Although the AVIFile functions and macros work with any RIFF file, this overview demonstrates their use with AVI files only.</span></span> <span data-ttu-id="d1528-111">AVI-файлы обычно представляют собой временные файлы, используемые в макросах и функциях Авифиле.</span><span class="sxs-lookup"><span data-stu-id="d1528-111">AVI files are typically the time-based files used with the AVIFile macros and functions.</span></span>

 

<span data-ttu-id="d1528-112">Функции и макросы Авифиле содержатся в библиотеке динамической компоновки.</span><span class="sxs-lookup"><span data-stu-id="d1528-112">AVIFile functions and macros are contained in a dynamic-link library.</span></span> <span data-ttu-id="d1528-113">Чтобы инициализировать библиотеку, используйте функцию [**авифилеинит**](/windows/desktop/api/Vfw/nf-vfw-avifileinit) .</span><span class="sxs-lookup"><span data-stu-id="d1528-113">To initialize the library, use the [**AVIFileInit**](/windows/desktop/api/Vfw/nf-vfw-avifileinit) function.</span></span> <span data-ttu-id="d1528-114">После инициализации библиотеки можно использовать любую из функций или макросов Авифиле.</span><span class="sxs-lookup"><span data-stu-id="d1528-114">After you initialize the library, you can use any of the AVIFile functions or macros.</span></span> <span data-ttu-id="d1528-115">Чтобы освободить библиотеку, используйте функцию [**авифиликсит**](/windows/desktop/api/Vfw/nf-vfw-avifileexit) .</span><span class="sxs-lookup"><span data-stu-id="d1528-115">To release the library, use the [**AVIFileExit**](/windows/desktop/api/Vfw/nf-vfw-avifileexit) function.</span></span> <span data-ttu-id="d1528-116">Авифиле поддерживает подсчет ссылок на приложения, использующие библиотеку, но не на тех, для которых она была выпущена.</span><span class="sxs-lookup"><span data-stu-id="d1528-116">AVIFile maintains a reference count of the applications that are using the library, but not those that have released it.</span></span> <span data-ttu-id="d1528-117">Приложения должны сбалансировать каждое использование **авифилеинит** с помощью вызова **авифиликсит** , чтобы полностью освободить библиотеку после того, как каждое приложение завершит его использование.</span><span class="sxs-lookup"><span data-stu-id="d1528-117">Your applications should balance each use of **AVIFileInit** with a call to **AVIFileExit** to completely release the library after each application finishes using it.</span></span>

 

 




