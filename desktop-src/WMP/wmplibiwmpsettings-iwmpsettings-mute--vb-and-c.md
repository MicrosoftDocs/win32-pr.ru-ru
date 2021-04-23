---
title: Свойство отключения Ивмпсеттингс
description: Свойство выкл. Получает или задает значение, указывающее, отключено ли звуковое сопровождение.
ms.assetid: d99e47db-70cc-41e0-aca9-b765b075e7b4
keywords:
- выключить проигрыватель Windows Media Player
- отключить звук свойства проигрыватель Windows Media Player, интерфейс Ивмпсеттингс
- Интерфейс Ивмпсеттингс Windows Media Player, выключение свойства
topic_type:
- apiref
api_name:
- IWMPSettings.mute
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67518bb9a6eccee13e4cc262f37341d30689439e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718175"
---
# <a name="iwmpsettingsmute-property"></a><span data-ttu-id="f22c8-106">Свойство Ивмпсеттингс:: выкл.</span><span class="sxs-lookup"><span data-stu-id="f22c8-106">IWMPSettings::mute property</span></span>

<span data-ttu-id="f22c8-107">Свойство **выкл** . Получает или задает значение, указывающее, отключено ли звуковое сопровождение.</span><span class="sxs-lookup"><span data-stu-id="f22c8-107">The **mute** property gets or sets a value indicating whether audio is muted.</span></span>

## <a name="syntax"></a><span data-ttu-id="f22c8-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f22c8-108">Syntax</span></span>


```CSharp
public System.Boolean mute {get; set;}
```


```VB

Public Property mute As System.Boolean
```





## <a name="property-value"></a><span data-ttu-id="f22c8-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="f22c8-109">Property value</span></span>

<span data-ttu-id="f22c8-110">Значение **System. Boolean** , указывающее, отключено ли звуковое сопровождение.</span><span class="sxs-lookup"><span data-stu-id="f22c8-110">A **System.Boolean** value indicating whether audio is muted.</span></span> <span data-ttu-id="f22c8-111">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="f22c8-111">The default is **false**.</span></span>

## <a name="examples"></a><span data-ttu-id="f22c8-112">Примеры</span><span class="sxs-lookup"><span data-stu-id="f22c8-112">Examples</span></span>

<span data-ttu-id="f22c8-113">В следующем примере создается флажок и переключается на свойство выкл. при изменении состояния флажка значение параметра **выключить** звук будет отключено.</span><span class="sxs-lookup"><span data-stu-id="f22c8-113">The following example creates a check box, and toggles the **mute** property to mute and un-mute audio when the checked state of the box is changed.</span></span> <span data-ttu-id="f22c8-114">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="f22c8-114">**AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void Mute_CheckStateChanged(object sender, System.EventArgs e)
{
    System.Windows.Forms.CheckBox Mute = (System.Windows.Forms.CheckBox)sender;

    // Change the check box text depending on the checked state.
    Mute.Text = Mute.Checked ? "Un-mute Audio" : Mute.Text = "Mute Audio";

    // Use the checked state to set the mute property. 
    player.settings.mute = Mute.Checked;
}
```


```VB

Public Sub Mute_CheckStateChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles Mute.CheckStateChanged

    Dim cb As System.Windows.Forms.CheckBox = sender

    &#39;  Change the check box text depending on the checked state.
    If (cb.Checked) Then

        cb.Text = &quot;Un-mute Audio&quot;

    Else

        cb.Text = &quot;Mute Audio&quot;

    End If

    &#39;  Use the checked state to set the mute property. 
    player.settings.mute = cb.Checked

End Sub
```





## <a name="requirements"></a><span data-ttu-id="f22c8-115">Требования</span><span class="sxs-lookup"><span data-stu-id="f22c8-115">Requirements</span></span>



| <span data-ttu-id="f22c8-116">Требование</span><span class="sxs-lookup"><span data-stu-id="f22c8-116">Requirement</span></span> | <span data-ttu-id="f22c8-117">Значение</span><span class="sxs-lookup"><span data-stu-id="f22c8-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f22c8-118">Версия</span><span class="sxs-lookup"><span data-stu-id="f22c8-118">Version</span></span><br/>   | <span data-ttu-id="f22c8-119">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="f22c8-119">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="f22c8-120">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f22c8-120">Namespace</span></span><br/> | <span data-ttu-id="f22c8-121">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="f22c8-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="f22c8-122">Сборка</span><span class="sxs-lookup"><span data-stu-id="f22c8-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f22c8-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="f22c8-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f22c8-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f22c8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f22c8-125">**Интерфейс Ивмпсеттингс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="f22c8-125">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f22c8-126">**Ивмпсеттингс. rate (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="f22c8-126">**IWMPSettings.rate (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> </dl>

 

 





