---
title: External. accountType
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. Использование этой функции вне контекста Интернет-магазина не поддерживается. Свойство accountType Извлекает тип учетной записи текущего пользователя.
ms.assetid: 4fb6de90-a32d-4483-bbae-b23cbff93bd5
keywords:
- External. accountType, проигрыватель Windows Media
topic_type:
- apiref
api_name:
- External.accountType
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16fce659f38af19157536a4bf763362c35fc9dfa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695210"
---
# <a name="externalaccounttype"></a><span data-ttu-id="c7a71-106">External. accountType</span><span class="sxs-lookup"><span data-stu-id="c7a71-106">External.accountType</span></span>

> [!Note]  
> <span data-ttu-id="c7a71-107">В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах.</span><span class="sxs-lookup"><span data-stu-id="c7a71-107">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="c7a71-108">Использование этой функции вне контекста Интернет-магазина не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c7a71-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="c7a71-109">Свойство **accountType** Извлекает тип учетной записи текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="c7a71-109">The **accountType** property retrieves the account type of the current user.</span></span>

``` syntax
window.external.accountType
      
```

## <a name="possible-values"></a><span data-ttu-id="c7a71-110">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="c7a71-110">Possible Values</span></span>

<span data-ttu-id="c7a71-111">Это свойство является **строкой** только для чтения, представляющей тип учетной записи.</span><span class="sxs-lookup"><span data-stu-id="c7a71-111">This property is a read-only **String** that represents the account type.</span></span> <span data-ttu-id="c7a71-112">Строки, представляющие различные типы учетных записей, определяются Интернет-магазином.</span><span class="sxs-lookup"><span data-stu-id="c7a71-112">Strings that represent various account types are defined by the online store.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7a71-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c7a71-113">Remarks</span></span>

<span data-ttu-id="c7a71-114">Это свойство извлекает тип учетной записи путем вызова метода [ивмпконтентпартнер:: жетконтентпартнеринфо](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcontentpartnerinfo) , который реализуется подключаемым модулем Интернет-магазина.</span><span class="sxs-lookup"><span data-stu-id="c7a71-114">This property retrieves the account type by calling the [IWMPContentPartner::GetContentPartnerInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcontentpartnerinfo) method, which is implemented by the online store's plug-in.</span></span> <span data-ttu-id="c7a71-115">Если текущий пользователь вошел в Интернет-магазин или подключаемый модуль кэширует учетные данные пользователя, метод **жетконтентпартнеринфо** может определить тип учетной записи пользователя и вернуть его проигрывателю Windows Media.</span><span class="sxs-lookup"><span data-stu-id="c7a71-115">If the current user is logged in to the online store or the plug-in has cached the user's credentials, the **getContentPartnerInfo** method can determine the user's account type and return it to Windows Media Player.</span></span> <span data-ttu-id="c7a71-116">Тип учетной записи — это строка, которую проигрыватель Windows Media не интерпретирует.</span><span class="sxs-lookup"><span data-stu-id="c7a71-116">The account type is a string that Windows Media Player does not interpret.</span></span> <span data-ttu-id="c7a71-117">Вместо этого проигрыватель Windows Media передает строку из подключаемого модуля интернет-магазина в скрипт на странице обнаружения в Интернет-магазине.</span><span class="sxs-lookup"><span data-stu-id="c7a71-117">Rather, Windows Media Player passes the string from the online store's plug-in to the script on the online store's discovery page.</span></span>

<span data-ttu-id="c7a71-118">Если текущий пользователь не вошел в Интернет-магазин, а подключаемый модуль интернет-магазина не имеет кэшированных учетных данных для пользователя, это свойство получает любую строку, возвращаемую методом **жетконтентпартнеринфо** в этой ситуации.</span><span class="sxs-lookup"><span data-stu-id="c7a71-118">If the current user is not logged in to the online store and the online store's plug-in does not have cached credentials for the user, this property retrieves whatever string the **getContentPartnerInfo** method returns in that situation.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7a71-119">Требования</span><span class="sxs-lookup"><span data-stu-id="c7a71-119">Requirements</span></span>



| <span data-ttu-id="c7a71-120">Требование</span><span class="sxs-lookup"><span data-stu-id="c7a71-120">Requirement</span></span> | <span data-ttu-id="c7a71-121">Значение</span><span class="sxs-lookup"><span data-stu-id="c7a71-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c7a71-122">Версия</span><span class="sxs-lookup"><span data-stu-id="c7a71-122">Version</span></span><br/> | <span data-ttu-id="c7a71-123">Проигрыватель Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="c7a71-123">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="c7a71-124">DLL</span><span class="sxs-lookup"><span data-stu-id="c7a71-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="c7a71-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7a71-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7a71-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c7a71-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7a71-127">**Внешний объект для Интернет-магазинов типа 1**</span><span class="sxs-lookup"><span data-stu-id="c7a71-127">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="c7a71-128">**External. Усерлогжедин**</span><span class="sxs-lookup"><span data-stu-id="c7a71-128">**External.userLoggedIn**</span></span>](external-userloggedin.md)
</dt> </dl>

 

 





