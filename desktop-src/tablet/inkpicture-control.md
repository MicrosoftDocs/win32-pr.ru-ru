---
description: Справочный раздел по элементу управления InkPicture для планшетных ПК.
ms.assetid: 1ced9779-dae5-4f9a-8a68-b2c0d041d5b4
title: Элемент управления InkPicture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ded5295d48e4bb14b3c0d83713f33939a360cff4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664297"
---
# <a name="inkpicture-control"></a><span data-ttu-id="0c6e9-103">Элемент управления InkPicture</span><span class="sxs-lookup"><span data-stu-id="0c6e9-103">InkPicture Control</span></span>

<span data-ttu-id="0c6e9-104">Элемент управления [InkPicture](inkpicture-control-reference.md) позволяет поместить изображение (JPG, BMP, PNG или GIF) в приложение, к которому пользователи могут добавлять рукописные данные.</span><span class="sxs-lookup"><span data-stu-id="0c6e9-104">The [InkPicture](inkpicture-control-reference.md) control enables you to place an image (.jpg, .bmp, .png, or .gif format) in an application that users can add ink to.</span></span> <span data-ttu-id="0c6e9-105">Он предназначен для сценариев, в которых рукописный ввод не должен распознаться как текст, но хранится в виде рукописного текста.</span><span class="sxs-lookup"><span data-stu-id="0c6e9-105">It is intended for scenarios in which ink need not be recognized as text but is stored as ink.</span></span>

<span data-ttu-id="0c6e9-106">Пользователи добавляют рукописный ввод в прозрачный слой с помощью пера.</span><span class="sxs-lookup"><span data-stu-id="0c6e9-106">Users add ink to a transparent layer using a pen.</span></span> <span data-ttu-id="0c6e9-107">Пользователи могут изменять размер окна [InkPicture](inkpicture-control-reference.md) без потери каких-либо сведений о рукописных данных, даже если они обрезаны при изменении размера.</span><span class="sxs-lookup"><span data-stu-id="0c6e9-107">Users can re-size an [InkPicture](inkpicture-control-reference.md) window without losing any ink information, even if the ink is cropped when re-sizing.</span></span>

<span data-ttu-id="0c6e9-108">Элемент управления [InkPicture](inkpicture-control-reference.md) включает базовую поддержку печати; Тем не менее, вам нужно реализовать предварительный просмотр или другие расширенные возможности печати.</span><span class="sxs-lookup"><span data-stu-id="0c6e9-108">The [InkPicture](inkpicture-control-reference.md) control includes basic printing support; however, it is up to you to implement print preview or other advanced printing capabilities.</span></span>

<span data-ttu-id="0c6e9-109">Управляемая (платформа .NET Framework) реализация [InkPicture](/previous-versions/ms583740(v=vs.100)) наследуется от класса [PictureBox](/dotnet/api/system.windows.forms.picturebox?view=netcore-3.1) .</span><span class="sxs-lookup"><span data-stu-id="0c6e9-109">The managed (.NET Framework) implementation of [InkPicture](/previous-versions/ms583740(v=vs.100)) inherits from the [PictureBox](/dotnet/api/system.windows.forms.picturebox?view=netcore-3.1) class.</span></span>

<span data-ttu-id="0c6e9-110">По умолчанию рукописные данные выделяются черным цветом, если они не находятся в режиме высокой контрастности. в противном случае для него задается значение текущий параметр системного цвета (ЦВЕТовая \_ WINDOWTEXT).</span><span class="sxs-lookup"><span data-stu-id="0c6e9-110">By default, ink is colored black if not in high-contrast mode; otherwise, it is set to the current system color setting (COLOR\_WINDOWTEXT) value.</span></span> <span data-ttu-id="0c6e9-111">Кроме того, по умолчанию [**фиттокурве**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_fittocurve) имеет **значение false**.</span><span class="sxs-lookup"><span data-stu-id="0c6e9-111">Also, by default [**FitToCurve**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_fittocurve) is **FALSE**.</span></span>

<span data-ttu-id="0c6e9-112">В элементе управления [InkPicture](inkpicture-control-reference.md) используйте объект [**Ink**](inkdisp-class.md) для загрузки и сохранения рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="0c6e9-112">Within the [InkPicture](inkpicture-control-reference.md) control, use the [**Ink**](inkdisp-class.md) object to load and save ink.</span></span>

> [!Note]  
> <span data-ttu-id="0c6e9-113">Если задать для [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode) значение **Delete** или **SELECT**, активируются другие события (например, событие [**Stroke**](inkpicture-stroke.md) ).</span><span class="sxs-lookup"><span data-stu-id="0c6e9-113">When you set the [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode) to **Delete** or **Select**, other events (such as the [**Stroke**](inkpicture-stroke.md) event) are triggered.</span></span> <span data-ttu-id="0c6e9-114">Эти события полезны, если требуется реализовать собственные режимы удаления или выбора.</span><span class="sxs-lookup"><span data-stu-id="0c6e9-114">These events are useful if you want to implement your own delete or select modes.</span></span>

 

<span data-ttu-id="0c6e9-115">Подробные справочные сведения о элементе управления [InkPicture](inkpicture-control-reference.md) см. в разделе InkPicture.</span><span class="sxs-lookup"><span data-stu-id="0c6e9-115">For detailed reference information about the [InkPicture](inkpicture-control-reference.md) control, see InkPicture.</span></span>

<span data-ttu-id="0c6e9-116">В следующих разделах подробно описано использование элемента управления [InkPicture](inkpicture-control-reference.md) :</span><span class="sxs-lookup"><span data-stu-id="0c6e9-116">The following sections detail the use of the [InkPicture](inkpicture-control-reference.md) control:</span></span>

-   [<span data-ttu-id="0c6e9-117">Работа с изображениями</span><span class="sxs-lookup"><span data-stu-id="0c6e9-117">Working with Pictures</span></span>](working-with-pictures.md)
-   [<span data-ttu-id="0c6e9-118">Использование функции InkPicture в более ранних версиях Windows</span><span class="sxs-lookup"><span data-stu-id="0c6e9-118">Using InkPicture on Earlier Versions of Windows</span></span>](using-inkpicture-on-earlier-versions-of-windows.md)

 

 
