---
description: Windows GDI+ предоставляет классы Image и Bitmap для хранения изображений и управления ими.
ms.assetid: fcd7f3d9-8bad-44f8-8c9c-c2f5df4a7241
title: Использование матрицы цветов для преобразования одного цвета
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db56d0a64c36c08a5415d76e3fb184158d473268
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104566876"
---
# <a name="using-a-color-matrix-to-transform-a-single-color"></a><span data-ttu-id="f657e-103">Использование матрицы цветов для преобразования одного цвета</span><span class="sxs-lookup"><span data-stu-id="f657e-103">Using a Color Matrix to Transform a Single Color</span></span>

<span data-ttu-id="f657e-104">Windows GDI+ предоставляет классы [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) и [**Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) для хранения изображений и управления ими.</span><span class="sxs-lookup"><span data-stu-id="f657e-104">Windows GDI+ provides the [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) and [**Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) classes for storing and manipulating images.</span></span> <span data-ttu-id="f657e-105">Объекты **Image** и **Bitmap** хранят цвет каждого пикселя в виде 32-разрядного числа: по 8 бит для красного, зеленого, синего и альфа.</span><span class="sxs-lookup"><span data-stu-id="f657e-105">**Image** and **Bitmap** objects store the color of each pixel as a 32-bit number: 8 bits each for red, green, blue, and alpha.</span></span> <span data-ttu-id="f657e-106">Каждый из четырех компонентов — это число от 0 до 255, где 0 означает отсутствие интенсивности и 255, представляющие полную интенсивность.</span><span class="sxs-lookup"><span data-stu-id="f657e-106">Each of the four components is a number from 0 through 255, with 0 representing no intensity and 255 representing full intensity.</span></span> <span data-ttu-id="f657e-107">Альфа-компонент задает прозрачность цвета: 0 является полностью прозрачным, а 255 — полностью непрозрачным.</span><span class="sxs-lookup"><span data-stu-id="f657e-107">The alpha component specifies the transparency of the color: 0 is fully transparent, and 255 is fully opaque.</span></span>

<span data-ttu-id="f657e-108">Цветовой вектор — это 4-элементный кортеж из формы (красный, зеленый, синий, альфа).</span><span class="sxs-lookup"><span data-stu-id="f657e-108">A color vector is a 4-tuple of the form (red, green, blue, alpha).</span></span> <span data-ttu-id="f657e-109">Например, цветовой вектор (0, 255, 0, 255) представляет непрозрачный цвет, который не имеет красного или синего цвета, но имеет зеленый в полной интенсивности.</span><span class="sxs-lookup"><span data-stu-id="f657e-109">For example, the color vector (0, 255, 0, 255) represents an opaque color that has no red or blue, but has green at full intensity.</span></span>

<span data-ttu-id="f657e-110">Другое соглашение для представления цветов использует число 1 для максимальной интенсивности и число 0 для минимальной интенсивности.</span><span class="sxs-lookup"><span data-stu-id="f657e-110">Another convention for representing colors uses the number 1 for maximum intensity and the number 0 for minimum intensity.</span></span> <span data-ttu-id="f657e-111">При использовании этого соглашения цвет, описанный в предыдущем абзаце, будет представлен вектором (0, 1, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="f657e-111">Using that convention, the color described in the preceding paragraph would be represented by the vector (0, 1, 0, 1).</span></span> <span data-ttu-id="f657e-112">При выполнении преобразований цветов в GDI+ используется соглашение 1 как полная интенсивность.</span><span class="sxs-lookup"><span data-stu-id="f657e-112">GDI+ uses the convention of 1 as full intensity when it performs color transformations.</span></span>

<span data-ttu-id="f657e-113">Линейные преобразования (вращение, масштабирование и т. д.) можно применять к цветным векторам путем умножения на матрицу размером 4 × 4.</span><span class="sxs-lookup"><span data-stu-id="f657e-113">You can apply linear transformations (rotation, scaling, and the like) to color vectors by multiplying by a 4 ×4 matrix.</span></span> <span data-ttu-id="f657e-114">Однако нельзя использовать матрицу размером 4 × 4 для перевода (нелинейной).</span><span class="sxs-lookup"><span data-stu-id="f657e-114">However, you cannot use a 4 ×4 matrix to perform a translation (nonlinear).</span></span> <span data-ttu-id="f657e-115">При добавлении фиктивной пятой координаты (например, номер 1) к каждому цветному вектору можно использовать матрицу 5 × 5 для применения любого сочетания линейных преобразований и переводов.</span><span class="sxs-lookup"><span data-stu-id="f657e-115">If you add a dummy fifth coordinate (for example, the number 1) to each of the color vectors, you can use a 5 ×5 matrix to apply any combination of linear transformations and translations.</span></span> <span data-ttu-id="f657e-116">Преобразование, состоящее из линейного преобразования, за которым следует перевод, называется аффинное преобразованием.</span><span class="sxs-lookup"><span data-stu-id="f657e-116">A transformation consisting of a linear transformation followed by a translation is called an affine transformation.</span></span> <span data-ttu-id="f657e-117">Матрица 5 × 5, представляющая аффинное преобразование, называется однородной матрицей для преобразования в 4 пространства.</span><span class="sxs-lookup"><span data-stu-id="f657e-117">A 5 ×5 matrix that represents an affine transformation is called a homogeneous matrix for a 4-space transformation.</span></span> <span data-ttu-id="f657e-118">Элемент в пятой и пятой столбцах однородной матрицы 5 × 5 должен быть равен 1, а все остальные записи в пятом столбце должны быть равны 0.</span><span class="sxs-lookup"><span data-stu-id="f657e-118">The element in the fifth row and fifth column of a 5 ×5 homogeneous matrix must be 1, and all of the other entries in the fifth column must be 0.</span></span>

<span data-ttu-id="f657e-119">Например, предположим, что вы хотите начать с цвета (0,2, 0,0, 0,4, 1,0) и применить следующие преобразования:</span><span class="sxs-lookup"><span data-stu-id="f657e-119">For example, suppose you want to start with the color (0.2, 0.0, 0.4, 1.0) and apply the following transformations:</span></span>

1.  <span data-ttu-id="f657e-120">Двойное значение красного компонента</span><span class="sxs-lookup"><span data-stu-id="f657e-120">Double the red component</span></span>
2.  <span data-ttu-id="f657e-121">Добавление 0,2 к красному, зеленому и синему компонентам</span><span class="sxs-lookup"><span data-stu-id="f657e-121">Add 0.2 to the red, green, and blue components</span></span>

<span data-ttu-id="f657e-122">Следующее умножение матрицы будет выполнять пару преобразований в указанном порядке.</span><span class="sxs-lookup"><span data-stu-id="f657e-122">The following matrix multiplication will perform the pair of transformations in the order listed.</span></span>

![Иллюстрация, демонстрирующая 5x1 матрицу чисел, умноженную на матрицу 5x5 для создания новой матрицы 5x1](images/recoloring01.png)

<span data-ttu-id="f657e-124">Элементы цветовой матрицы индексируются (отсчитывается от нуля) по строке, а затем по столбцу.</span><span class="sxs-lookup"><span data-stu-id="f657e-124">The elements of a color matrix are indexed (zero-based) by row and then column.</span></span> <span data-ttu-id="f657e-125">Например, запись в пятой строке и третьем столбце матрицы M обозначается M \[ 4 \] \[ 2 \] .</span><span class="sxs-lookup"><span data-stu-id="f657e-125">For example, the entry in the fifth row and third column of matrix M is denoted by M\[4\]\[2\].</span></span>

<span data-ttu-id="f657e-126">Матрица идентификации 5 × 5 (показана на следующем рисунке) имеет 1 на диагонали и на нулях везде.</span><span class="sxs-lookup"><span data-stu-id="f657e-126">The 5 ×5 identity matrix (shown in the following illustration) has 1s on the diagonal and 0s everywhere else.</span></span> <span data-ttu-id="f657e-127">При умножении вектора цвета на матрицу идентификаторов цветовой вектор не изменяется.</span><span class="sxs-lookup"><span data-stu-id="f657e-127">If you multiply a color vector by the identity matrix, the color vector does not change.</span></span> <span data-ttu-id="f657e-128">Чтобы создать матрицу преобразования цвета, удобно начать с матрицы идентификаторов и внести небольшое изменение, которое приведет к желаемому преобразованию.</span><span class="sxs-lookup"><span data-stu-id="f657e-128">A convenient way to form the matrix of a color transformation is to start with the identity matrix and make a small change that produces the desired transformation.</span></span>

![Иллюстрация, демонстрирующая матрицу удостоверений 5x5; 1S в верхнем левом углу влево и вправо по диагонали и в любом месте](images/recoloring02.png)

<span data-ttu-id="f657e-130">Более подробное описание матриц и преобразований см. в разделе [системы координат и преобразования](-gdiplus-coordinate-systems-and-transformations-about.md).</span><span class="sxs-lookup"><span data-stu-id="f657e-130">For a more detailed discussion of matrices and transformations, see [Coordinate Systems and Transformations](-gdiplus-coordinate-systems-and-transformations-about.md).</span></span>

<span data-ttu-id="f657e-131">В следующем примере берется изображение, которое имеет один цвет (0,2, 0,0, 0,4, 1,0), и применяется преобразование, описанное в предыдущих абзацах.</span><span class="sxs-lookup"><span data-stu-id="f657e-131">The following example takes an image that is all one color (0.2, 0.0, 0.4, 1.0) and applies the transformation described in the preceding paragraphs.</span></span>


```
Image            image(L"InputColor.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   2.0f, 0.0f, 0.0f, 0.0f, 0.0f,
   0.0f, 1.0f, 0.0f, 0.0f, 0.0f,
   0.0f, 0.0f, 1.0f, 0.0f, 0.0f,
   0.0f, 0.0f, 0.0f, 1.0f, 0.0f,
   0.2f, 0.2f, 0.2f, 0.0f, 1.0f};
   
imageAttributes.SetColorMatrix(
   &colorMatrix, 
   ColorMatrixFlagsDefault,
   ColorAdjustTypeBitmap);
   
graphics.DrawImage(&image, 10, 10);

graphics.DrawImage(
   &image, 
   Rect(120, 10, width, height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle 
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel,
   &imageAttributes);
```



<span data-ttu-id="f657e-132">На следующем рисунке показано исходное изображение слева и преобразованное изображение справа.</span><span class="sxs-lookup"><span data-stu-id="f657e-132">The following illustration shows the original image on the left and the transformed image on the right.</span></span>

![<span data-ttu-id="f657e-133">Иллюстрация, на которой показан прямоугольник, заполненный темным сплошным цветом, а затем один, заполненный светлым сплошным цветом</span><span class="sxs-lookup"><span data-stu-id="f657e-133">illustration showing a rectangle filled by a dark solid color and then one filled by a lighter solid color</span></span> ](images/colortrans1.png)

<span data-ttu-id="f657e-134">Код в предыдущем примере использует следующие шаги для выполнения перекрашивания.</span><span class="sxs-lookup"><span data-stu-id="f657e-134">The code in the preceding example uses the following steps to perform the recoloring:</span></span>

1.  <span data-ttu-id="f657e-135">Инициализируйте структуру [**КолорМатрикс**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix) .</span><span class="sxs-lookup"><span data-stu-id="f657e-135">Initialize a [**ColorMatrix**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix) structure.</span></span>
2.  <span data-ttu-id="f657e-136">Создайте объект [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) и передайте адрес структуры [**КолорМатрикс**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix) методу [**ImageAttributes:: сетколорматрикс**](/windows/win32/api/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setcolormatrix) объекта **ImageAttributes** .</span><span class="sxs-lookup"><span data-stu-id="f657e-136">Create an [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) object and pass the address of the [**ColorMatrix**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix) structure to the [**ImageAttributes::SetColorMatrix**](/windows/win32/api/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setcolormatrix) method of the **ImageAttributes** object.</span></span>
3.  <span data-ttu-id="f657e-137">Передайте адрес объекта [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) методу [методов DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)) объекта [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="f657e-137">Pass the address of the [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) object to the [DrawImage Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)) method of a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span>

 

 



