---
title: Предыдущий метод Ивмпконтролс
description: Предыдущий метод устанавливает предыдущий элемент списка воспроизведения в качестве текущего элемента.
ms.assetid: 380524f5-e8b6-45c4-9f6c-3dbb49b1ac9f
keywords:
- Предыдущий метод проигрывателя Windows Media
- Предыдущий метод проигрыватель Windows Media Player, интерфейс Ивмпконтролс
- Интерфейс Ивмпконтролс Windows Media Player, предыдущий метод
topic_type:
- apiref
api_name:
- IWMPControls.previous
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 823038205a026afb7141491f562698eb60515a5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689295"
---
# <a name="iwmpcontrolsprevious-method"></a><span data-ttu-id="a7c93-106">Ивмпконтролс: метод:p Предыдущая</span><span class="sxs-lookup"><span data-stu-id="a7c93-106">IWMPControls::previous method</span></span>

<span data-ttu-id="a7c93-107">**Предыдущий** метод устанавливает предыдущий элемент списка воспроизведения в качестве текущего элемента.</span><span class="sxs-lookup"><span data-stu-id="a7c93-107">The **previous** method sets the previous item in the playlist as the current item.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7c93-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a7c93-108">Syntax</span></span>


```CSharp
public void previous();
```


```VB

Public Sub previous()
Implements IWMPControls.previous
```





## <a name="parameters"></a><span data-ttu-id="a7c93-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a7c93-109">Parameters</span></span>

<span data-ttu-id="a7c93-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="a7c93-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a7c93-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a7c93-111">Return value</span></span>

<span data-ttu-id="a7c93-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="a7c93-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7c93-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a7c93-113">Remarks</span></span>

<span data-ttu-id="a7c93-114">Если список воспроизведения находится в первой записи при вызове **предыдущего** , последняя запись списка воспроизведения станет текущей.</span><span class="sxs-lookup"><span data-stu-id="a7c93-114">If the playlist is on the first entry when **previous** is invoked, the last entry in the playlist will become the current one.</span></span>

## <a name="examples"></a><span data-ttu-id="a7c93-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="a7c93-115">Examples</span></span>

<span data-ttu-id="a7c93-116">В следующем примере функция **Previous** используется для перехода к предыдущему элементу в текущем списке воспроизведения в ответ на событие щелчка кнопки.</span><span class="sxs-lookup"><span data-stu-id="a7c93-116">The following example uses **previous** to move to the previous item in the current playlist in response to the Click event of a button.</span></span> <span data-ttu-id="a7c93-117">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="a7c93-117">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void previousButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid. 
    if (controls.get_isAvailable("previous"))
    {
        controls.previous();
    }
}
```


```VB

Public Sub previousButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles previousButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid. 
    If (controls.isAvailable(&quot;previous&quot;)) Then

        controls.previous()

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="a7c93-118">Требования</span><span class="sxs-lookup"><span data-stu-id="a7c93-118">Requirements</span></span>



| <span data-ttu-id="a7c93-119">Требование</span><span class="sxs-lookup"><span data-stu-id="a7c93-119">Requirement</span></span> | <span data-ttu-id="a7c93-120">Значение</span><span class="sxs-lookup"><span data-stu-id="a7c93-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7c93-121">Версия</span><span class="sxs-lookup"><span data-stu-id="a7c93-121">Version</span></span><br/>   | <span data-ttu-id="a7c93-122">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="a7c93-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="a7c93-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a7c93-123">Namespace</span></span><br/> | <span data-ttu-id="a7c93-124">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="a7c93-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="a7c93-125">Сборка</span><span class="sxs-lookup"><span data-stu-id="a7c93-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a7c93-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="a7c93-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7c93-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a7c93-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7c93-128">**Интерфейс Ивмпконтролс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="a7c93-128">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a7c93-129">**Ивмпконтролс. Next (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="a7c93-129">**IWMPControls.next (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-next--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a7c93-130">**Ивмпконтролс. останавливаться (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="a7c93-130">**IWMPControls.stop (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> </dl>

 

 





