---
description: Из шести стандартных режимов сопоставления один из них зависит от устройства ( \_ текст мм), а оставшиеся пять (mm \_ ХИЕНГЛИШ, mm \_ лоенглиш, MM \_ HIMETRIC, mm \_ лометрик и мм \_ твипов) являются независимыми от устройства.
ms.assetid: 722df020-edf2-4763-b58c-3e29fa7007db
title: Стандартные режимы сопоставления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f252f587e98a739306a84450a1d9669ed21873cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984852"
---
# <a name="predefined-mapping-modes"></a><span data-ttu-id="c9a60-103">Стандартные режимы сопоставления</span><span class="sxs-lookup"><span data-stu-id="c9a60-103">Predefined Mapping Modes</span></span>

<span data-ttu-id="c9a60-104">Из шести стандартных режимов сопоставления один из них зависит от устройства ( \_ текст мм), а оставшиеся пять (mm \_ ХИЕНГЛИШ, mm \_ лоенглиш, MM \_ HIMETRIC, mm \_ лометрик и мм \_ твипов) являются независимыми от устройства.</span><span class="sxs-lookup"><span data-stu-id="c9a60-104">Of the six predefined mapping modes, one is device dependent (MM\_TEXT) and the remaining five (MM\_HIENGLISH, MM\_LOENGLISH, MM\_HIMETRIC, MM\_LOMETRIC, and MM\_TWIPS) are device independent.</span></span>

<span data-ttu-id="c9a60-105">Режим сопоставления по умолчанию — текст в виде MM \_ .</span><span class="sxs-lookup"><span data-stu-id="c9a60-105">The default mapping mode is MM\_TEXT.</span></span> <span data-ttu-id="c9a60-106">Одна логическая единица равна одному пикселю.</span><span class="sxs-lookup"><span data-stu-id="c9a60-106">One logical unit equals one pixel.</span></span> <span data-ttu-id="c9a60-107">Положительный x — справа, а положительный y — нет.</span><span class="sxs-lookup"><span data-stu-id="c9a60-107">Positive x is to the right, and positive y is down.</span></span> <span data-ttu-id="c9a60-108">Этот режим напрямую сопоставляется с системой координат устройства.</span><span class="sxs-lookup"><span data-stu-id="c9a60-108">This mode maps directly to the device's coordinate system.</span></span> <span data-ttu-id="c9a60-109">Сопоставление "логический к физическому" включает только смещение в x и y, которое определяется окнами, управляемыми приложением, и источниками окна просмотра.</span><span class="sxs-lookup"><span data-stu-id="c9a60-109">The logical-to-physical mapping involves only an offset in x and y that is defined by the application-controlled window and viewport origins.</span></span> <span data-ttu-id="c9a60-110">Для окна просмотра и экстентов окна задано значение 1, что позволяет создать сопоставление «один к одному».</span><span class="sxs-lookup"><span data-stu-id="c9a60-110">The viewport and window extents are all set to 1, creating a one-to-one mapping.</span></span>

<span data-ttu-id="c9a60-111">В приложениях, отображающих геометрические фигуры (круги, квадраты, многоугольники и т. д.), используется один из независимых от устройства режимов сопоставления.</span><span class="sxs-lookup"><span data-stu-id="c9a60-111">Applications that display geometric shapes (circles, squares, polygons, and so on) make use of one of the device-independent mapping modes.</span></span> <span data-ttu-id="c9a60-112">Например, при написании приложения для обеспечения возможностей создания диаграмм для программы электронной таблицы и необходимости гарантировать, что диаметр каждой круговой диаграммы составляет 2 дюйма, используйте \_ режим СОПОСТАВЛЕНИЯ mm лоенглиш и вызовите соответствующие функции для рисования и заполнения диаграммы.</span><span class="sxs-lookup"><span data-stu-id="c9a60-112">For example, if you are writing an application to provide charting capabilities for a spreadsheet program and want to guarantee that the diameter of each pie chart is 2 inches, use the MM\_LOENGLISH mapping mode and call the appropriate functions to draw and fill the chart.</span></span> <span data-ttu-id="c9a60-113">Задание MM \_ лоенглиш гарантирует, что диаметр диаграммы будет согласованным на любом дисплее или на принтере.</span><span class="sxs-lookup"><span data-stu-id="c9a60-113">Specifying MM\_LOENGLISH, guarantees that the diameter of the chart is consistent on any display or printer.</span></span> <span data-ttu-id="c9a60-114">Если \_ вместо mm лоенглиш используется текст mm \_ , то диаграмма, которая отображается циклически на дисплее VGA, будет выглядеть как эллиптическая на дисплее Ега и будет выглядеть очень маленькой на лазерном принтере 300 dpi (в точках на дюйм).</span><span class="sxs-lookup"><span data-stu-id="c9a60-114">If MM\_TEXT is used instead of MM\_LOENGLISH, a chart that appears circular on a VGA display would appear elliptical on an EGA display and would appear very small on a 300 dpi (dots per inch) laser printer.</span></span>

 

 



