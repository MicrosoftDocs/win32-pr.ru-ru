---
title: Ошибка. метод Help
description: Метод "Справка" открывает страницу веб-справки проигрывателя Windows Media для вывода дополнительных сведений о первой ошибке в очереди ошибок (нулевой индекс). | Ошибка. метод Help
ms.assetid: 79797b41-1d47-4347-aa47-c104f7f7fbaf
keywords:
- метод WebMethod проигрыватель Windows Media
- метод WebMethod Windows Media Player, класс Error
- Класс ошибок Windows Media Player, метод WebMethod
topic_type:
- apiref
api_name:
- Error.webHelp
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 862376be956bc8b37a778f5c9d1d2238c876208d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698970"
---
# <a name="errorwebhelp-method"></a><span data-ttu-id="08f3c-107">Ошибка. метод Help</span><span class="sxs-lookup"><span data-stu-id="08f3c-107">Error.webHelp method</span></span>

<span data-ttu-id="08f3c-108">Метод " **Справка** " открывает страницу веб-справки проигрывателя Windows Media для вывода дополнительных сведений о первой ошибке в очереди ошибок (нулевой индекс).</span><span class="sxs-lookup"><span data-stu-id="08f3c-108">The **webHelp** method launches the Windows Media Player Web Help page to display further information about the first error in the error queue (index zero).</span></span>

## <a name="syntax"></a><span data-ttu-id="08f3c-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="08f3c-109">Syntax</span></span>


```JScript
Error.webHelp()
```



## <a name="parameters"></a><span data-ttu-id="08f3c-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="08f3c-110">Parameters</span></span>

<span data-ttu-id="08f3c-111">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="08f3c-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="08f3c-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="08f3c-112">Return value</span></span>

<span data-ttu-id="08f3c-113">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="08f3c-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="08f3c-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="08f3c-114">Remarks</span></span>

<span data-ttu-id="08f3c-115">Страницы веб-справки всегда содержат последние и более подробные сведения об ошибках проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="08f3c-115">The Web Help pages always contain the latest and most detailed information about Windows Media Player errors.</span></span> <span data-ttu-id="08f3c-116">Этот метод автоматически передает другие сведения, необходимые для веб-справки, например используемую версию операционной системы.</span><span class="sxs-lookup"><span data-stu-id="08f3c-116">This method automatically transfers the other information needed by Web Help, such as the operating system version being used.</span></span>

<span data-ttu-id="08f3c-117">Чтобы получить доступ к страницам веб-справки напрямую, используйте следующий код ошибки и ссылки центра поддержки.</span><span class="sxs-lookup"><span data-stu-id="08f3c-117">To access the Web Help pages directly, use the following error code and support center links.</span></span>

-   [<span data-ttu-id="08f3c-118">Сведения о коде ошибки проигрывателя Windows Media</span><span class="sxs-lookup"><span data-stu-id="08f3c-118">Windows Media Player Error Code Information</span></span>](https://support.microsoft.com/kb/886273)
-   [<span data-ttu-id="08f3c-119">Центр решений проигрывателя Windows Media</span><span class="sxs-lookup"><span data-stu-id="08f3c-119">Windows Media Player Solution Center</span></span>](https://support.microsoft.com/ph/7763#tab0)

<span data-ttu-id="08f3c-120">**Проигрыватель Windows Media 10 Mobile:** Этот метод всегда выполняется, но не выполняет требуемую операцию.</span><span class="sxs-lookup"><span data-stu-id="08f3c-120">**Windows Media Player 10 Mobile:** This method always succeeds, but does not perform the intended operation.</span></span>

## <a name="examples"></a><span data-ttu-id="08f3c-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="08f3c-121">Examples</span></span>

<span data-ttu-id="08f3c-122">В следующем примере создается элемент кнопки HTML, который запускает страницу веб-справки проигрывателя Microsoft Windows Media.</span><span class="sxs-lookup"><span data-stu-id="08f3c-122">The following example creates an HTML BUTTON element that launches the Microsoft Windows Media Player Web Help page.</span></span> <span data-ttu-id="08f3c-123">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="08f3c-123">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  
       NAME = "WHBUTTON"  
       VALUE = "More Info"

OnClick = "Player.error.webHelp();

">

```



## <a name="requirements"></a><span data-ttu-id="08f3c-124">Требования</span><span class="sxs-lookup"><span data-stu-id="08f3c-124">Requirements</span></span>



| <span data-ttu-id="08f3c-125">Требование</span><span class="sxs-lookup"><span data-stu-id="08f3c-125">Requirement</span></span> | <span data-ttu-id="08f3c-126">Значение</span><span class="sxs-lookup"><span data-stu-id="08f3c-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="08f3c-127">Версия</span><span class="sxs-lookup"><span data-stu-id="08f3c-127">Version</span></span><br/> | <span data-ttu-id="08f3c-128">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="08f3c-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="08f3c-129">DLL</span><span class="sxs-lookup"><span data-stu-id="08f3c-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="08f3c-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08f3c-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08f3c-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="08f3c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08f3c-132">**Объект Error**</span><span class="sxs-lookup"><span data-stu-id="08f3c-132">**Error Object**</span></span>](error-object.md)
</dt> </dl>

 

 





