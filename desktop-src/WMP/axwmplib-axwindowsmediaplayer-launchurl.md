---
title: Аксвиндовсмедиаплайер. Лаунчурл, метод
description: Метод Лаунчурл отправляет URL-адрес браузеру пользователя по умолчанию для подготовки к просмотру. | Аксвиндовсмедиаплайер. Лаунчурл, метод
ms.assetid: 3e8dfdbb-b5ad-44ea-97a6-e860386b7fb4
keywords:
- Лаунчурл метод Windows Media Player
- Лаунчурл метод Windows Media Player, класс Аксвиндовсмедиаплайер
- Класс Аксвиндовсмедиаплайер Windows Media Player, метод Лаунчурл
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.launchURL
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27fe8e544bb14b119785b26b9cb5be5cdad48015
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699026"
---
# <a name="axwindowsmediaplayerlaunchurl-method"></a><span data-ttu-id="eae36-107">Аксвиндовсмедиаплайер. Лаунчурл, метод</span><span class="sxs-lookup"><span data-stu-id="eae36-107">AxWindowsMediaPlayer.launchURL method</span></span>

<span data-ttu-id="eae36-108">Метод Лаунчурл отправляет URL-адрес браузеру пользователя по умолчанию для подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="eae36-108">The launchURL method sends a URL to the user's default browser to be rendered.</span></span>

## <a name="syntax"></a><span data-ttu-id="eae36-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eae36-109">Syntax</span></span>


```CSharp
public void launchURL(
  System.String bstrURL
);
```


```VB

Public Sub launchURL( _
  ByVal bstrURL As System.String _
)
```





## <a name="parameters"></a><span data-ttu-id="eae36-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="eae36-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eae36-111">*бструрл*</span><span class="sxs-lookup"><span data-stu-id="eae36-111">*bstrURL*</span></span> 
</dt> <dd>

<span data-ttu-id="eae36-112">**Строка System. String** , которая является URL-адресом для запуска.</span><span class="sxs-lookup"><span data-stu-id="eae36-112">The **System.String** that is the URL to launch.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eae36-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="eae36-113">Return value</span></span>

<span data-ttu-id="eae36-114">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="eae36-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="eae36-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eae36-115">Remarks</span></span>

<span data-ttu-id="eae36-116">Этот метод открывает только веб-страницы с использованием протоколов HTTP или HTTPS.</span><span class="sxs-lookup"><span data-stu-id="eae36-116">This method only opens webpages using the HTTP or HTTPS protocols.</span></span>

## <a name="examples"></a><span data-ttu-id="eae36-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="eae36-117">Examples</span></span>

<span data-ttu-id="eae36-118">В следующем примере создается кнопка, которая при нажатии отображает веб-сайт Майкрософт в новом окне браузера.</span><span class="sxs-lookup"><span data-stu-id="eae36-118">The following example creates a button that, when clicked, displays the Microsoft website in a new browser window.</span></span> <span data-ttu-id="eae36-119">Объект Аксвмплиб. Аксвиндовсмедиаплайер представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="eae36-119">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
private void goToMS_Click(object sender, System.EventArgs e)
{
    // Open the Microsoft website. 
    player.launchURL("https://www.microsoft.com");
}
```


```VB

Public Sub goToMS_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles goToMS.Click

    &#39; Open the Microsoft website. 
    player.launchURL(&quot;https://www.microsoft.com&quot;)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="eae36-120">Требования</span><span class="sxs-lookup"><span data-stu-id="eae36-120">Requirements</span></span>



| <span data-ttu-id="eae36-121">Требование</span><span class="sxs-lookup"><span data-stu-id="eae36-121">Requirement</span></span> | <span data-ttu-id="eae36-122">Значение</span><span class="sxs-lookup"><span data-stu-id="eae36-122">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eae36-123">Версия</span><span class="sxs-lookup"><span data-stu-id="eae36-123">Version</span></span><br/>   | <span data-ttu-id="eae36-124">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="eae36-124">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="eae36-125">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="eae36-125">Namespace</span></span><br/> | <span data-ttu-id="eae36-126">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="eae36-126">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="eae36-127">Сборка</span><span class="sxs-lookup"><span data-stu-id="eae36-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="eae36-128"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="eae36-128"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eae36-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eae36-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eae36-130">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="eae36-130">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





