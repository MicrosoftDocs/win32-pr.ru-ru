---
title: Ивмперрор, метод
description: Метод "Справка" открывает страницу веб-справки проигрывателя Windows Media для вывода дополнительных сведений о первой ошибке в очереди ошибок (нулевой индекс). | Ивмперрор, метод
ms.assetid: 30fc765a-04b2-44e5-99d8-0b4720ccbb25
keywords:
- метод WebMethod проигрыватель Windows Media
- метод WebMethod проигрыватель Windows Media Player, интерфейс Ивмперрор
- Интерфейс Ивмперрор Windows Media Player, метод WebMethod
topic_type:
- apiref
api_name:
- IWMPError.webHelp
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c9b0cd48d45ac5e5e5d77d0150b8acdf13347e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708534"
---
# <a name="iwmperrorwebhelp-method"></a><span data-ttu-id="2e249-107">Метод Ивмперрор:: Help</span><span class="sxs-lookup"><span data-stu-id="2e249-107">IWMPError::webHelp method</span></span>

<span data-ttu-id="2e249-108">Метод " **Справка** " открывает страницу веб-справки проигрывателя Windows Media для вывода дополнительных сведений о первой ошибке в очереди ошибок (нулевой индекс).</span><span class="sxs-lookup"><span data-stu-id="2e249-108">The **webHelp** method launches the Windows Media Player Web Help page to display further information about the first error in the error queue (index zero).</span></span>

## <a name="syntax"></a><span data-ttu-id="2e249-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2e249-109">Syntax</span></span>


```CSharp
public void webHelp();
```


```VB

Public Sub webHelp()
Implements IWMPError.webHelp
```





## <a name="parameters"></a><span data-ttu-id="2e249-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="2e249-110">Parameters</span></span>

<span data-ttu-id="2e249-111">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="2e249-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2e249-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2e249-112">Return value</span></span>

<span data-ttu-id="2e249-113">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="2e249-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e249-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2e249-114">Remarks</span></span>

<span data-ttu-id="2e249-115">Страницы веб-справки всегда содержат последние и более подробные сведения об ошибках проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="2e249-115">The Web Help pages always contain the latest and most detailed information about Windows Media Player errors.</span></span> <span data-ttu-id="2e249-116">Этот метод автоматически передает другие сведения, необходимые для веб-справки, например используемую версию операционной системы.</span><span class="sxs-lookup"><span data-stu-id="2e249-116">This method automatically transfers the other information needed by Web Help, such as the operating system version being used.</span></span>

<span data-ttu-id="2e249-117">Чтобы получить доступ к страницам веб-справки напрямую, используйте следующий код ошибки и ссылки центра поддержки:</span><span class="sxs-lookup"><span data-stu-id="2e249-117">To access the Web Help pages directly, use the following error code and support center links:</span></span>

-   [<span data-ttu-id="2e249-118">Сведения о коде ошибки проигрывателя Windows Media</span><span class="sxs-lookup"><span data-stu-id="2e249-118">Windows Media Player Error Code Information</span></span>](https://support.microsoft.com/kb/886273)
-   [<span data-ttu-id="2e249-119">Центр решений проигрывателя Windows Media</span><span class="sxs-lookup"><span data-stu-id="2e249-119">Windows Media Player Solution Center</span></span>](https://support.microsoft.com/ph/7763#tab0)

## <a name="examples"></a><span data-ttu-id="2e249-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="2e249-120">Examples</span></span>

<span data-ttu-id="2e249-121">В следующем примере создается кнопка, которая запускает страницу веб-справки проигрывателя Microsoft Windows Media в браузере.</span><span class="sxs-lookup"><span data-stu-id="2e249-121">The following example creates a button that launches the Microsoft Windows Media Player Web Help page in the browser.</span></span> <span data-ttu-id="2e249-122">Объект Аксвмплиб. Аксвиндовсмедиаплайер представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="2e249-122">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
private void webHelpButton_Click(object sender, System.EventArgs e)
{
    // Launch the Microsoft Windows Media Player Web Help page in the browser.
    player.Error.webHelp();
}
```


```VB

Public Sub webHelpButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles webHelpButton.Click

    &#39; Launch the Microsoft Windows Media Player Web Help page in the browser.
    player.Error.webHelp()

End Sub
```





## <a name="requirements"></a><span data-ttu-id="2e249-123">Требования</span><span class="sxs-lookup"><span data-stu-id="2e249-123">Requirements</span></span>



| <span data-ttu-id="2e249-124">Требование</span><span class="sxs-lookup"><span data-stu-id="2e249-124">Requirement</span></span> | <span data-ttu-id="2e249-125">Значение</span><span class="sxs-lookup"><span data-stu-id="2e249-125">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e249-126">Версия</span><span class="sxs-lookup"><span data-stu-id="2e249-126">Version</span></span><br/>   | <span data-ttu-id="2e249-127">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="2e249-127">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="2e249-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2e249-128">Namespace</span></span><br/> | <span data-ttu-id="2e249-129">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="2e249-129">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="2e249-130">Сборка</span><span class="sxs-lookup"><span data-stu-id="2e249-130">Assembly</span></span><br/>  | <dl> <span data-ttu-id="2e249-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="2e249-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e249-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2e249-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e249-133">**Интерфейс Ивмперрор (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="2e249-133">**IWMPError Interface (VB and C#)**</span></span>](iwmperror--vb-and-c.md)
</dt> </dl>

 

 





