---
title: Ивмперроритем errorDescription, свойство
description: Свойство errorDescription Возвращает описание ошибки.
ms.assetid: a9914c24-1d10-422a-bcba-80be9fb85108
keywords:
- Проигрыватель Windows Media для свойства errorDescription
- errorDescription свойство проигрывателя Windows Media Player, интерфейс Ивмперроритем
- Интерфейс Ивмперроритем Windows Media Player, свойство errorDescription
topic_type:
- apiref
api_name:
- IWMPErrorItem.errorDescription
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8725099d1ce49eae8f378b2571dc4030f60611e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708530"
---
# <a name="iwmperroritemerrordescription-property"></a><span data-ttu-id="38a5d-106">Свойство Ивмперроритем:: errorDescription</span><span class="sxs-lookup"><span data-stu-id="38a5d-106">IWMPErrorItem::errorDescription property</span></span>

<span data-ttu-id="38a5d-107">Свойство **errorDescription** Возвращает описание ошибки.</span><span class="sxs-lookup"><span data-stu-id="38a5d-107">The **errorDescription** property gets a description of the error.</span></span>

## <a name="syntax"></a><span data-ttu-id="38a5d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="38a5d-108">Syntax</span></span>


```CSharp
public System.String errorDescription {get; set;}
```


```VB

Public ReadOnly Property errorDescription As System.String
```





## <a name="property-value"></a><span data-ttu-id="38a5d-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="38a5d-109">Property value</span></span>

<span data-ttu-id="38a5d-110">**Строка System. String** , которая является описанием ошибки.</span><span class="sxs-lookup"><span data-stu-id="38a5d-110">A **System.String** that is the error description.</span></span>

## <a name="remarks"></a><span data-ttu-id="38a5d-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="38a5d-111">Remarks</span></span>

<span data-ttu-id="38a5d-112">Если выбрано отображение настраиваемых сообщений об ошибках, следует задать для **ивмпсеттингс. енаблиррордиалогс** **значение false** .</span><span class="sxs-lookup"><span data-stu-id="38a5d-112">You should set **IWMPSettings.enableErrorDialogs** to **false** if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="38a5d-113">Примеры</span><span class="sxs-lookup"><span data-stu-id="38a5d-113">Examples</span></span>

<span data-ttu-id="38a5d-114">В следующем примере для вывода описания ошибки пользователю используется **errorDescription** в обработчике событий ошибки.</span><span class="sxs-lookup"><span data-stu-id="38a5d-114">The following example uses **errorDescription** in an Error event handler to display the error description to the user.</span></span> <span data-ttu-id="38a5d-115">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="38a5d-115">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void player_ErrorEvent_errorDescription(object sender, System.EventArgs e)
{
    // Get the error description for the first error item.
    string errDesc = player.Error.get_Item(0).errorDescription;

    // Display the error description.
    System.Windows.Forms.MessageBox.Show("Error: " + errDesc);
}
```


```VB

Public Sub player_ErrorEvent_errorDescription(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Get the error description for the first error item.
    Dim errDesc As String = player.Error.Item(0).errorDescription

    &#39; Display the error description.
    System.Windows.Forms.MessageBox.Show(&quot;Error: &quot; + errDesc)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="38a5d-116">Требования</span><span class="sxs-lookup"><span data-stu-id="38a5d-116">Requirements</span></span>



| <span data-ttu-id="38a5d-117">Требование</span><span class="sxs-lookup"><span data-stu-id="38a5d-117">Requirement</span></span> | <span data-ttu-id="38a5d-118">Значение</span><span class="sxs-lookup"><span data-stu-id="38a5d-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38a5d-119">Версия</span><span class="sxs-lookup"><span data-stu-id="38a5d-119">Version</span></span><br/>   | <span data-ttu-id="38a5d-120">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="38a5d-120">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="38a5d-121">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="38a5d-121">Namespace</span></span><br/> | <span data-ttu-id="38a5d-122">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="38a5d-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="38a5d-123">Сборка</span><span class="sxs-lookup"><span data-stu-id="38a5d-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="38a5d-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="38a5d-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38a5d-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="38a5d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38a5d-126">**Интерфейс Ивмперроритем (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="38a5d-126">**IWMPErrorItem Interface (VB and C#)**</span></span>](iwmperroritem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="38a5d-127">**Ивмпсеттингс. Енаблиррордиалогс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="38a5d-127">**IWMPSettings.enableErrorDialogs (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> </dl>

 

 





