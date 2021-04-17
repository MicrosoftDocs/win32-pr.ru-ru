---
title: Аксвиндовсмедиаплайер. versionInfo, свойство
description: Свойство versionInfo возвращает значение, указывающее версию проигрывателя Windows Media.
ms.assetid: e128bec5-1ae9-4710-800e-4f97df362909
keywords:
- Проигрыватель Windows Media для свойства versionInfo
- versionInfo свойства проигрывателя Windows Media Player, класс Аксвиндовсмедиаплайер
- Класс Аксвиндовсмедиаплайер Windows Media Player, свойство versionInfo
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.versionInfo
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2f759c2aedb19e21c4b7d90f3634141e4c37ec8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698848"
---
# <a name="axwindowsmediaplayerversioninfo-property"></a><span data-ttu-id="5cf3b-106">Аксвиндовсмедиаплайер. versionInfo, свойство</span><span class="sxs-lookup"><span data-stu-id="5cf3b-106">AxWindowsMediaPlayer.versionInfo property</span></span>

<span data-ttu-id="5cf3b-107">Свойство versionInfo возвращает значение, указывающее версию проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="5cf3b-107">The versionInfo property gets a value that specifies the version of the Windows Media Player.</span></span>

<span data-ttu-id="5cf3b-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="5cf3b-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5cf3b-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5cf3b-109">Syntax</span></span>


```CSharp
public System.String versionInfo {get;}
```


```VB

Public ReadOnly Property versionInfo As System.String
```





## <a name="property-value"></a><span data-ttu-id="5cf3b-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="5cf3b-110">Property value</span></span>

<span data-ttu-id="5cf3b-111">Строка System. String, которая является сведениями о версии в следующем формате: "*X*. 0,0. *Yyyy*"где *X* представляет основной номер версии, а *yyyy* — номер сборки.</span><span class="sxs-lookup"><span data-stu-id="5cf3b-111">A System.String that is the version information in the following format: "*X*.0.0.*YYYY*" where *X* represents the major version number and *YYYY* represents the build number.</span></span>

## <a name="examples"></a><span data-ttu-id="5cf3b-112">Примеры</span><span class="sxs-lookup"><span data-stu-id="5cf3b-112">Examples</span></span>

<span data-ttu-id="5cf3b-113">В следующем примере создается кнопка, которая при нажатии отображает окно сообщения, содержащее сведения о версии проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="5cf3b-113">The following example creates a button that, when clicked, displays a message box containing the version information for Windows Media Player.</span></span> <span data-ttu-id="5cf3b-114">Объект Аксвмплиб. Аксвиндовсмедиаплайер представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="5cf3b-114">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
private void showVersion_Click(object sender, System.EventArgs e)
{
    // Build the message containing the version info. 
    string message = ("Windows Media Player Version: " + player.versionInfo);

    // Display the message. 
    System.Windows.Forms.MessageBox.Show(message);
}
```


```VB

Public Sub showVersion_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles showVersion.Click

    &#39; Build the message containing the version info. 
    Dim message As String = (&quot;Windows Media Player Version: &quot; + player.versionInfo)

    &#39; Display the message. 
    System.Windows.Forms.MessageBox.Show(message)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="5cf3b-115">Требования</span><span class="sxs-lookup"><span data-stu-id="5cf3b-115">Requirements</span></span>



| <span data-ttu-id="5cf3b-116">Требование</span><span class="sxs-lookup"><span data-stu-id="5cf3b-116">Requirement</span></span> | <span data-ttu-id="5cf3b-117">Значение</span><span class="sxs-lookup"><span data-stu-id="5cf3b-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5cf3b-118">Версия</span><span class="sxs-lookup"><span data-stu-id="5cf3b-118">Version</span></span><br/>   | <span data-ttu-id="5cf3b-119">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="5cf3b-119">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="5cf3b-120">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="5cf3b-120">Namespace</span></span><br/> | <span data-ttu-id="5cf3b-121">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="5cf3b-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="5cf3b-122">Сборка</span><span class="sxs-lookup"><span data-stu-id="5cf3b-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="5cf3b-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="5cf3b-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5cf3b-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5cf3b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cf3b-125">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="5cf3b-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





