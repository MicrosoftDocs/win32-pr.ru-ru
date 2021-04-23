---
title: Ивмпнетворк Буфферингтиме, свойство
description: Свойство Буфферингтиме Возвращает или задает время (в миллисекундах), выделенное для буферизации входящих данных перед началом воспроизведения.
ms.assetid: b5936b21-a17b-4801-a5fc-c6d6521e05aa
keywords:
- Проигрыватель Windows Media для свойства Буфферингтиме
- Буфферингтиме свойство проигрывателя Windows Media Player, интерфейс Ивмпнетворк
- Интерфейс Ивмпнетворк Windows Media Player, свойство Буфферингтиме
topic_type:
- apiref
api_name:
- IWMPNetwork.bufferingTime
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8594d53797b028dd74a8ef11cb8f2fa64b3654cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694479"
---
# <a name="iwmpnetworkbufferingtime-property"></a><span data-ttu-id="7eb0e-106">Свойство Ивмпнетворк:: Буфферингтиме</span><span class="sxs-lookup"><span data-stu-id="7eb0e-106">IWMPNetwork::bufferingTime property</span></span>

<span data-ttu-id="7eb0e-107">Свойство **буфферингтиме** Возвращает или задает время (в миллисекундах), выделенное для буферизации входящих данных перед началом воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="7eb0e-107">The **bufferingTime** property gets or sets the amount of time in milliseconds allocated for buffering incoming data before playback begins.</span></span>

## <a name="syntax"></a><span data-ttu-id="7eb0e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7eb0e-108">Syntax</span></span>


```CSharp
public System.Int32 bufferingTime {get; set;}
```


```VB

Public Property bufferingTime As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="7eb0e-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="7eb0e-109">Property value</span></span>

<span data-ttu-id="7eb0e-110">Значение **System. Int32** , которое является временем буферизации в миллисекундах, которое в диапазоне от нуля до 60 000 со значением по умолчанию 5 000.</span><span class="sxs-lookup"><span data-stu-id="7eb0e-110">A **System.Int32** that is the buffering time in milliseconds, which ranges from zero to 60,000 with a default value of 5,000.</span></span>

## <a name="examples"></a><span data-ttu-id="7eb0e-111">Примеры</span><span class="sxs-lookup"><span data-stu-id="7eb0e-111">Examples</span></span>

<span data-ttu-id="7eb0e-112">В следующем примере кода используется **буфферингтиме** для указания количества секунд, выделенных для буферизации входящих данных.</span><span class="sxs-lookup"><span data-stu-id="7eb0e-112">The following code example uses **bufferingTime** to specify the number of seconds allocated for buffering incoming data.</span></span> <span data-ttu-id="7eb0e-113">Текстовое поле позволяет пользователю ввести новое значение для **буфферингтиме**, а свойство обновляется в ответ на событие щелчка кнопки.</span><span class="sxs-lookup"><span data-stu-id="7eb0e-113">A text box allows the user to enter a new value for **bufferingTime**, and the property is updated in response to the Click event of a button.</span></span> <span data-ttu-id="7eb0e-114">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="7eb0e-114">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void setBufTime_Click(object sender, System.EventArgs e)
{
    // Retrieve input from the user and convert it to an integer.
    int newTime = System.Convert.ToInt32(bufText.Text);

    // Test whether the integer is within the valid range. 
    if (newTime >= 0 & newTime <= 60) 
    {
        // Set the new bufferingTime in miliseconds.
        player.network.bufferingTime = (newTime * 1000);
    }
    else
    {
        System.Windows.Forms.MessageBox.Show("Buffering time must be between 0 and 60.");
    }
}
```


```VB

Public Sub setBufTime_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setBufTime.Click

    &#39; Retrieve input from the user and convert it to an integer.
    Dim newTime As Integer = System.Convert.ToInt32(bufText.Text)

    &#39; Test whether the integer is within the valid range. 
    If (newTime >= 0 And newTime <= 60) Then

        &#39; Set the new bufferingTime in miliseconds.
        player.network.bufferingTime = (newTime * 1000)

    Else

        System.Windows.Forms.MessageBox.Show(&quot;Buffering time must be between 0 and 60.&quot;)

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="7eb0e-115">Требования</span><span class="sxs-lookup"><span data-stu-id="7eb0e-115">Requirements</span></span>



| <span data-ttu-id="7eb0e-116">Требование</span><span class="sxs-lookup"><span data-stu-id="7eb0e-116">Requirement</span></span> | <span data-ttu-id="7eb0e-117">Значение</span><span class="sxs-lookup"><span data-stu-id="7eb0e-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7eb0e-118">Версия</span><span class="sxs-lookup"><span data-stu-id="7eb0e-118">Version</span></span><br/>   | <span data-ttu-id="7eb0e-119">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="7eb0e-119">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="7eb0e-120">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7eb0e-120">Namespace</span></span><br/> | <span data-ttu-id="7eb0e-121">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="7eb0e-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="7eb0e-122">Сборка</span><span class="sxs-lookup"><span data-stu-id="7eb0e-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="7eb0e-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="7eb0e-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7eb0e-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7eb0e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7eb0e-125">**Интерфейс Ивмпнетворк (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="7eb0e-125">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





