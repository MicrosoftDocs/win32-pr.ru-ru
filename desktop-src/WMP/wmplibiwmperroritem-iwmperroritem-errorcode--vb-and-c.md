---
title: Ивмперроритем errorCode, свойство
description: Свойство errorCode получает текущий код ошибки.
ms.assetid: 00719067-685d-4ef2-9eec-72c7892fcdb9
keywords:
- Свойство errorCode проигрыватель Windows Media Player
- Свойство errorCode проигрыватель Windows Media Player, интерфейс Ивмперроритем
- Интерфейс Ивмперроритем Windows Media Player, свойство errorCode
topic_type:
- apiref
api_name:
- IWMPErrorItem.errorCode
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f284d5655fc1f4007695a1f681c744a9c5c6fc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708531"
---
# <a name="iwmperroritemerrorcode-property"></a><span data-ttu-id="47499-106">Ивмперроритем:: errorCode, свойство</span><span class="sxs-lookup"><span data-stu-id="47499-106">IWMPErrorItem::errorCode property</span></span>

<span data-ttu-id="47499-107">Свойство **ErrorCode** получает текущий код ошибки.</span><span class="sxs-lookup"><span data-stu-id="47499-107">The **errorCode** property gets the current error code.</span></span>

## <a name="syntax"></a><span data-ttu-id="47499-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="47499-108">Syntax</span></span>


```CSharp
public System.Int32 errorCode {get; set;}
```


```VB

Public ReadOnly Property errorCode As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="47499-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="47499-109">Property value</span></span>

<span data-ttu-id="47499-110">Объект **System. Int32** , который является кодом ошибки.</span><span class="sxs-lookup"><span data-stu-id="47499-110">A **System.Int32** that is the error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="47499-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="47499-111">Remarks</span></span>

<span data-ttu-id="47499-112">Если выбрано отображение настраиваемых сообщений об ошибках, следует задать для **ивмпсеттингс. енаблиррордиалогс** **значение false** .</span><span class="sxs-lookup"><span data-stu-id="47499-112">You should set **IWMPSettings.enableErrorDialogs** to **false** if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="47499-113">Примеры</span><span class="sxs-lookup"><span data-stu-id="47499-113">Examples</span></span>

<span data-ttu-id="47499-114">В следующем примере **ErrorCode** используется в обработчике событий ошибки для вывода кода ошибки для пользователя.</span><span class="sxs-lookup"><span data-stu-id="47499-114">The following example uses **errorCode** in an Error event handler to display the error code to the user.</span></span> <span data-ttu-id="47499-115">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="47499-115">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void player_ErrorEvent_errorCode(object sender, System.EventArgs e)
{
    // Get the error code for the first error item.
    int errCode = player.Error.get_Item(0).errorCode;

    // Display the error code.
    System.Windows.Forms.MessageBox.Show("Error number: " + errCode.ToString());
}
```


```VB

Public Sub player_ErrorEvent_errorCode(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Get the error code for the first error item.
    Dim errCode As Integer = player.Error.Item(0).errorCode

    &#39; Display the error code.
    System.Windows.Forms.MessageBox.Show(&quot;Error number: &quot; + errCode.ToString())

End Sub
```





## <a name="requirements"></a><span data-ttu-id="47499-116">Требования</span><span class="sxs-lookup"><span data-stu-id="47499-116">Requirements</span></span>



| <span data-ttu-id="47499-117">Требование</span><span class="sxs-lookup"><span data-stu-id="47499-117">Requirement</span></span> | <span data-ttu-id="47499-118">Значение</span><span class="sxs-lookup"><span data-stu-id="47499-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47499-119">Версия</span><span class="sxs-lookup"><span data-stu-id="47499-119">Version</span></span><br/>   | <span data-ttu-id="47499-120">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="47499-120">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="47499-121">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="47499-121">Namespace</span></span><br/> | <span data-ttu-id="47499-122">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="47499-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="47499-123">Сборка</span><span class="sxs-lookup"><span data-stu-id="47499-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="47499-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="47499-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47499-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="47499-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47499-126">**Интерфейс Ивмперроритем (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="47499-126">**IWMPErrorItem Interface (VB and C#)**</span></span>](iwmperroritem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="47499-127">**Ивмпсеттингс. Енаблиррордиалогс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="47499-127">**IWMPSettings.enableErrorDialogs (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> </dl>

 

 





