---
title: Структуры — Стосерве
description: Собумага упаковывает цвет, ширину и координаты пера в структуры ИНКДАТА и сохраняет их в динамически выделенном массиве, который управляется в памяти.
ms.assetid: 25e68c39-5306-4ad6-85dd-a8a5e256abf0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9868f38d7915185b8d3511bd1bf6faa9c7a1e1b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986376"
---
# <a name="structures---stoserve"></a><span data-ttu-id="94da4-103">Структуры — Стосерве</span><span class="sxs-lookup"><span data-stu-id="94da4-103">Structures - StoServe</span></span>

<span data-ttu-id="94da4-104">Собумага упаковывает цвет, ширину и координаты пера в структуры **инкдата** и сохраняет их в динамически выделенном массиве, который управляется в памяти.</span><span class="sxs-lookup"><span data-stu-id="94da4-104">COPaper packages the pen color, width, and coordinates into **INKDATA** structures and stores them in a dynamically allocated array that it manages in memory.</span></span>

## <a name="inkdata-structure"></a><span data-ttu-id="94da4-105">Структура ИНКДАТА</span><span class="sxs-lookup"><span data-stu-id="94da4-105">INKDATA Structure</span></span>

<span data-ttu-id="94da4-106">Ниже приведены объявления для структуры **инкдата** из paper. H.</span><span class="sxs-lookup"><span data-stu-id="94da4-106">The following are the declarations for the **INKDATA** structure from PAPER.H.</span></span>

``` syntax
// The types of Ink Data.
#define INKTYPE_NONE  0
#define INKTYPE_START 1
#define INKTYPE_DRAW  2
#define INKTYPE_STOP  3

  // The Ink Data structure.
  typedef struct _INKDATA
  {
    SHORT nType;            // Ink Type.
    SHORT nX;               // X-coordinate of ink point.
    SHORT nY;               // Y-coordinate of ink point.
    SHORT nWidth;           // Ink line width in pixels.
    COLORREF crColor;       // Ink color.
  } INKDATA;
```

<span data-ttu-id="94da4-107">На динамический массив этих пакетов **инкдата** указывает m \_ паинкдата, член класса реализации [**ипапер**](ipaper-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="94da4-107">The dynamic array of these **INKDATA** packets is pointed to by m\_paInkData, a member of the [**IPaper**](ipaper-methods.md) implementation class.</span></span> <span data-ttu-id="94da4-108">Массив создается в методе **ипапер:: инитпапер** с начальным выделением.</span><span class="sxs-lookup"><span data-stu-id="94da4-108">The array is created within the **IPaper::InitPaper** method with an initial allocation.</span></span> <span data-ttu-id="94da4-109">Дополнительные сведения см. в описании метода **инитпапер** и закрытой служебной программы Некстслот реализации ЦИМПИПАПЕР в paper. H.</span><span class="sxs-lookup"><span data-stu-id="94da4-109">For details, see the **InitPaper** method and the private NextSlot utility method of the CImpIPaper implementation in PAPER.H.</span></span> <span data-ttu-id="94da4-110">Методы [**инкстарт**](inkstart-method.md), [**инкдрав**](inkdraw-method.md)и [**инкстоп**](cguipaper-methods.md) используют некстслот для получения новых слотов в массиве.</span><span class="sxs-lookup"><span data-stu-id="94da4-110">The [**InkStart**](inkstart-method.md), [**InkDraw**](inkdraw-method.md), and [**InkStop**](cguipaper-methods.md) methods use NextSlot to obtain new slots in the array.</span></span> <span data-ttu-id="94da4-111">Массив разворачивается динамически, Некстслот по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="94da4-111">The array is expanded dynamically by NextSlot as the need arises.</span></span>

<span data-ttu-id="94da4-112">Клиент вызывает метод [**ипапер:: Erase**](ipaper-methods.md) для стирания текущего документа.</span><span class="sxs-lookup"><span data-stu-id="94da4-112">The client calls the [**IPaper::Erase**](ipaper-methods.md) method to erase the current drawing.</span></span> <span data-ttu-id="94da4-113">Этот метод не перераспределяет массив. Он просто помечает все текущие рукописные данные как ИНКТИПЕ \_ None и сбрасывает индекс конца массива данных в нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="94da4-113">This method does not reallocate the array; it simply marks all current ink data as INKTYPE\_NONE and resets the array's end-of-data index to zero.</span></span>

<span data-ttu-id="94da4-114">Клиент вызывает методы [**ипапер:: Lock**](ipaper-methods.md) и **Unlock** для управления владельцем собумаги для рисования.</span><span class="sxs-lookup"><span data-stu-id="94da4-114">The client calls the [**IPaper::Lock**](ipaper-methods.md) and **Unlock** methods to manage ownership of COPaper for drawing.</span></span> <span data-ttu-id="94da4-115">Эти методы предоставляются для организации доступа между несколькими клиентами и рисунками, удерживаемыми в общей содокументе.</span><span class="sxs-lookup"><span data-stu-id="94da4-115">These methods are provided to organize access among multiple clients to the drawing held in a shared COPaper.</span></span>

## <a name="paper_properties-structure"></a><span data-ttu-id="94da4-116">\_Структура свойств бумаги</span><span class="sxs-lookup"><span data-stu-id="94da4-116">PAPER\_PROPERTIES Structure</span></span>

<span data-ttu-id="94da4-117">Клиент вызывает метод [**ипапер:: resize**](ipaper-methods.md) , чтобы дать сомнение о том, что пользователь изменяет размер текущего прямоугольника рисования.</span><span class="sxs-lookup"><span data-stu-id="94da4-117">The client calls the [**IPaper::Resize**](ipaper-methods.md) method to tell COPaper that the user resized the current drawing paper rectangle.</span></span> <span data-ttu-id="94da4-118">Данные о координатах хранятся в структуре **\_ свойств бумаги** , которая хранится вместе с рукописными данными, когда все бумажные данные хранятся в составном файле.</span><span class="sxs-lookup"><span data-stu-id="94da4-118">This coordinate data is kept in a **PAPER\_PROPERTIES** structure, which is stored with the ink data when all the paper data is stored in a compound file.</span></span>

<span data-ttu-id="94da4-119">Ниже приведено объявление **\_ свойств бумаги** из paper. H.</span><span class="sxs-lookup"><span data-stu-id="94da4-119">The following is the **PAPER\_PROPERTIES** declaration from PAPER.H.</span></span>

``` syntax
#define PAPER_TITLE_SIZE 64
  typedef struct _PAPER_PROPERTIES
  {
    LONG lInkDataVersion;
    LONG lInkArraySize;
    COLORREF crWinColor;
    RECT WinRect;
    WCHAR wszTitle[PAPER_TITLE_SIZE];
    WCHAR wszAuthor[PAPER_TITLE_SIZE];
    WCHAR wszReserved1[PAPER_TITLE_SIZE];
    WCHAR wszReserved2[PAPER_TITLE_SIZE];
  } PAPER_PROPERTIES;
```

<span data-ttu-id="94da4-120">Структура **\_ свойств бумаги** разработана таким образом, чтобы новые форматы данных рукописного ввода можно было добавлять в любое время по мере развития компонента дллпапер.</span><span class="sxs-lookup"><span data-stu-id="94da4-120">The **PAPER\_PROPERTIES** structure is designed so that new ink data formats can be added at any time as the DllPaper component evolves.</span></span> <span data-ttu-id="94da4-121">Интерфейс [**ипапер**](ipaper-methods.md) является достаточно общим, чтобы последующая версия компонента дллпапер могла сохранить другой формат рукописного ввода при реализации того же интерфейса **ипапер** .</span><span class="sxs-lookup"><span data-stu-id="94da4-121">The [**IPaper**](ipaper-methods.md) interface is general enough that a subsequent version of the DllPaper component may store a different ink data format while implementing the same **IPaper** interface.</span></span> <span data-ttu-id="94da4-122">Поскольку методы **ипапер** не зависят от конкретного формата рукописных данных, Новая версия компонента дллпапер, поддерживающая другой формат рукописных данных, может использовать этот же интерфейс.</span><span class="sxs-lookup"><span data-stu-id="94da4-122">Because the methods of **IPaper** do not depend on a specific ink data format, a new version of the DllPaper component that does support a different ink data format can use this same interface.</span></span>

<span data-ttu-id="94da4-123">Свойства бумаги, хранящиеся в составном файле, записывают текущий размер массива рукописных данных.</span><span class="sxs-lookup"><span data-stu-id="94da4-123">The paper properties stored in a compound file record the current size of the ink data array.</span></span> <span data-ttu-id="94da4-124">Затем можно выделить правильный размер массива, чтобы разместить данные рукописного ввода, считанные из файла.</span><span class="sxs-lookup"><span data-stu-id="94da4-124">The proper array size can then be allocated to accommodate the ink data read from the file.</span></span>

<span data-ttu-id="94da4-125">В **структуре \_ свойств бумаги** также хранится размер прямоугольника рисунка и цвет окна фона в области бумаги.</span><span class="sxs-lookup"><span data-stu-id="94da4-125">The **PAPER\_PROPERTIES** structure also stores the paper surface's drawing rectangle size and background window color.</span></span>

<span data-ttu-id="94da4-126">Хотя и не используется в  / примерах стосерве **стоклиен** , можно также сохранить заголовок рисунка и имя автора.</span><span class="sxs-lookup"><span data-stu-id="94da4-126">Though not used in the **StoServe**/**StoClien** samples, a drawing title and an author name can also be stored.</span></span>

<span data-ttu-id="94da4-127">Даты создания и даты последнего изменения не включены в эти свойства бумаги, так как интерфейс [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) , используемый для доступа к составным файлам, управляет этими сведениями.</span><span class="sxs-lookup"><span data-stu-id="94da4-127">Creation date and last modified dates are not included in these paper properties, because the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface used to access compound files manages this information.</span></span>

 

 




