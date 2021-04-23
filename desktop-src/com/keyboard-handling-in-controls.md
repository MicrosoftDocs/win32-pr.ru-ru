---
title: Обработка клавиатуры в элементах управления
description: Обработка клавиатуры в элементах управления
ms.assetid: 33affb3f-5d52-4ada-9751-0775b31a375e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f32610732ddbf88c6a587d5bc0fd7de1188152d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700703"
---
# <a name="keyboard-handling-in-controls"></a><span data-ttu-id="4ee92-103">Обработка клавиатуры в элементах управления</span><span class="sxs-lookup"><span data-stu-id="4ee92-103">Keyboard Handling in Controls</span></span>

<span data-ttu-id="4ee92-104">Настоятельно рекомендуется поддержка обработки клавиатуры для следующих функций, хотя она распознает, что она неприменима ко всем контейнерам.</span><span class="sxs-lookup"><span data-stu-id="4ee92-104">Keyboard handling support for the following functionality is strongly recommended, although it is recognized that it is not applicable to all containers.</span></span>

-   <span data-ttu-id="4ee92-105">Поддержка \_ бит состояния олемиск актсликелабел и олемиск \_ актсликебуттон.</span><span class="sxs-lookup"><span data-stu-id="4ee92-105">Support for OLEMISC\_ACTSLIKELABEL and OLEMISC\_ACTSLIKEBUTTON status bits.</span></span>
-   <span data-ttu-id="4ee92-106">Реализация свойства окружения DisplayAsDefault (если оно существует, оно может возвращать **значение false**).</span><span class="sxs-lookup"><span data-stu-id="4ee92-106">Implementing the DisplayAsDefault ambient property (if it exists, it can return **FALSE**).</span></span>
-   <span data-ttu-id="4ee92-107">Реализация обработки вкладок, включая последовательность табуляции.</span><span class="sxs-lookup"><span data-stu-id="4ee92-107">Implementing tab handling, including tab order.</span></span>

<span data-ttu-id="4ee92-108">Некоторые контейнеры будут использовать элементы управления ActiveX в традиционных сценариях составных документов.</span><span class="sxs-lookup"><span data-stu-id="4ee92-108">Some containers will use ActiveX controls in traditional compound document scenarios.</span></span> <span data-ttu-id="4ee92-109">Например, электронная таблица может позволить пользователю внедрить элемент управления ActiveX в лист.</span><span class="sxs-lookup"><span data-stu-id="4ee92-109">For example, a spreadsheet may allow a user to embed an ActiveX control into a worksheet.</span></span> <span data-ttu-id="4ee92-110">В таких сценариях контейнер будет выполнять обработку клавиатуры по-разному, так как интерфейс клавиатуры должен оставаться соответствующим ожиданиям пользователя электронной таблицы.</span><span class="sxs-lookup"><span data-stu-id="4ee92-110">In such scenarios, the container would do keyboard handling differently, because the keyboard interface should remain consistent with the user's expectations of a spreadsheet.</span></span> <span data-ttu-id="4ee92-111">Документация по таким продуктам должна информировать пользователей о различиях в обработке элементов управления в различных сценариях.</span><span class="sxs-lookup"><span data-stu-id="4ee92-111">Documentation for such products should inform users of differences in control handling in these different scenarios.</span></span> <span data-ttu-id="4ee92-112">Другие контейнеры должны правильно учитывать указанные выше функции, включая обработку назначенных клавиш.</span><span class="sxs-lookup"><span data-stu-id="4ee92-112">Other containers should endeavor to honor the above functionality correctly, including Mnemonic handling.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4ee92-113">См. также</span><span class="sxs-lookup"><span data-stu-id="4ee92-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ee92-114">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="4ee92-114">Containers</span></span>](containers.md)
</dt> </dl>

 

 




