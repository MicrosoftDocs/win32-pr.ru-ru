---
title: UI_PKEY_FontProperties_Size
description: Определяет свойство UI \_ PKEY \_ фонтпропертиес \_ size.
ms.assetid: bd426910-9852-48e1-91c8-b94be5ef7199
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ae991cfe5f91b4aca4fe0b49a7b7c547e71b0fb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105681382"
---
# <a name="ui_pkey_fontproperties_size"></a><span data-ttu-id="7cb13-103">\_ \_ Размер фонтпропертиес пользовательского интерфейса PKEY \_</span><span class="sxs-lookup"><span data-stu-id="7cb13-103">UI\_PKEY\_FontProperties\_Size</span></span>

<span data-ttu-id="7cb13-104">Определяет свойство UI \_ PKEY \_ фонтпропертиес \_ size.</span><span class="sxs-lookup"><span data-stu-id="7cb13-104">Identifies the UI\_PKEY\_FontProperties\_Size property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_Size
   shellPKey = UI_PKEY_FontProperties_Size
   formatID = 00000302-7363-696e-8441798acf5aebb7
   propID = 302
   typeInfo
      type = VT_DECIMAL
```

## <a name="remarks"></a><span data-ttu-id="7cb13-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7cb13-105">Remarks</span></span>

<span data-ttu-id="7cb13-106">\_ \_ Размер фонтпропертиес UI PKEY \_ используется приложением для запроса значения элемента управления **размером шрифта** .</span><span class="sxs-lookup"><span data-stu-id="7cb13-106">UI\_PKEY\_FontProperties\_Size is used by an application to query the value of the **Font size** control.</span></span>

<span data-ttu-id="7cb13-107">Допустимые значения для этого свойства в диапазоне от 1 до 9999 включительно.</span><span class="sxs-lookup"><span data-stu-id="7cb13-107">Valid values for this property range from 1 to 9999, inclusive.</span></span> <span data-ttu-id="7cb13-108">Если пользователь пытается ввести недопустимое значение, запись отклоняется, а элемент управления **размером шрифта** возвращается к последнему допустимому значению.</span><span class="sxs-lookup"><span data-stu-id="7cb13-108">If a user tries to enter an invalid value, the entry is rejected and the **Font size** control reverts to the last valid value.</span></span>

<span data-ttu-id="7cb13-109">Если приложение пытается установить размер шрифта программным образом до значения, находящегося за пределами допустимого диапазона, платформа Ribbon делает недействительными все свойства шрифта и устанавливает для элементов управления шрифтом (**Размер** и начертание **шрифта**) значение пустое или в состояние по умолчанию, где это необходимо.</span><span class="sxs-lookup"><span data-stu-id="7cb13-109">If an application attempts to set font size programmatically to a value outside the valid range, the Ribbon framework invalidates all font properties and sets the font controls (**Font size** and **Font face**) to blank or to their default state, where appropriate.</span></span>

<span data-ttu-id="7cb13-110">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="7cb13-110">The default value is 0.</span></span>

<span data-ttu-id="7cb13-111">Значение 0 указывает, что ни один размер одной точки не выбран (ни текст, ни выполнение хетероженеаусли размера текста).</span><span class="sxs-lookup"><span data-stu-id="7cb13-111">A value of 0 specifies that no single point size is selected (either no text, or a run of heterogeneously sized text, is selected).</span></span>

<span data-ttu-id="7cb13-112">Пользователь не может задать для элемента управления **размером шрифта** значение 0.</span><span class="sxs-lookup"><span data-stu-id="7cb13-112">A user cannot set the **Font size** control to 0.</span></span>

<span data-ttu-id="7cb13-113">Кроме 0, допустимые значения для \_ \_ диапазона размеров фонтпропертиес UI PKEY находятся \_ между *минимумфонтсизе* и *максимумфонтсизе* , как объявлено в разметке [элемента управления Font](windowsribbon-controls-fontcontrol.md) .</span><span class="sxs-lookup"><span data-stu-id="7cb13-113">Other than 0, valid values for UI\_PKEY\_FontProperties\_Size range between *MinimumFontSize* and *MaximumFontSize* as declared in the [Font Control](windowsribbon-controls-fontcontrol.md) markup.</span></span>

> [!Note]  
> <span data-ttu-id="7cb13-114">Элемент управления " **Размер шрифта** " имеет значение "пусто", если размер шрифта программным образом имеет значение 0, например при выделении хетероженеаусли размера текста.</span><span class="sxs-lookup"><span data-stu-id="7cb13-114">The **Font size** control is set to blank when the font size is programmatically set to 0, such as when a run of heterogeneously sized text is highlighted.</span></span>

 

<span data-ttu-id="7cb13-115">Если выбрано выполнение хетероженеаусли размера текста, приложение должно запрашивать [UI \_ PKEY \_ фонтпропертиес \_ делтасизе](windowsribbon-reference-properties-uipkey-fontproperties-deltasize.md) для захвата команд " **увеличить шрифт** " и " **Сжать шрифт** ".</span><span class="sxs-lookup"><span data-stu-id="7cb13-115">Where a run of heterogeneously sized text is selected, the application should query [UI\_PKEY\_FontProperties\_DeltaSize](windowsribbon-reference-properties-uipkey-fontproperties-deltasize.md) to capture **Grow font** and **Shrink font** commands.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7cb13-116">См. также</span><span class="sxs-lookup"><span data-stu-id="7cb13-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7cb13-117">Свойства элемента управления "Шрифт"</span><span class="sxs-lookup"><span data-stu-id="7cb13-117">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="7cb13-118">Элемент управления шрифтами</span><span class="sxs-lookup"><span data-stu-id="7cb13-118">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 




