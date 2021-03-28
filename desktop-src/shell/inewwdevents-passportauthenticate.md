---
description: Позволяет страницам на стороне сервера, размещенным в мастере, проверить, что пользователь прошел проверку подлинности с помощью учетная запись Майкрософт.
ms.assetid: 8b99eb84-c434-489a-b177-1e00f18d2dcc
title: Неввдевентс. Пасспортаусентикате, метод (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NewWDEvents.PassportAuthenticate
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 48e6cfbcbf525784fe33520702bbd9c05226f353
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103819041"
---
# <a name="newwdeventspassportauthenticate-method"></a><span data-ttu-id="270e4-103">Неввдевентс. Пасспортаусентикате, метод</span><span class="sxs-lookup"><span data-stu-id="270e4-103">NewWDEvents.PassportAuthenticate method</span></span>

<span data-ttu-id="270e4-104">Позволяет страницам на стороне сервера, размещенным в мастере, проверить, что пользователь прошел проверку подлинности с помощью учетная запись Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="270e4-104">Enables server-side pages hosted in a wizard to verify that the user has been authenticated through a Microsoft account.</span></span>

## <a name="syntax"></a><span data-ttu-id="270e4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="270e4-105">Syntax</span></span>


```JScript
bRetVal = NewWDEvents.PassportAuthenticate(
  bstrSignInUrl
)
```



## <a name="parameters"></a><span data-ttu-id="270e4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="270e4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="270e4-107">*бстрсигнинурл* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="270e4-107">*bstrSignInUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="270e4-108">Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="270e4-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="270e4-109">Строка, содержащая URL-адрес веб-страницы, которая перенаправляется на учетная запись Майкрософт Пользовательский интерфейс входа.</span><span class="sxs-lookup"><span data-stu-id="270e4-109">A string containing the URL of a webpage that redirects to the Microsoft account log on UI.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="270e4-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="270e4-110">Return value</span></span>

<span data-ttu-id="270e4-111">Тип: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="270e4-111">Type: **Boolean**</span></span>

<span data-ttu-id="270e4-112">Задайте значение **true** , если проверка подлинности выполнена, и **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="270e4-112">Set to **true** if authentication succeeds, **false** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="270e4-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="270e4-113">Remarks</span></span>

<span data-ttu-id="270e4-114">Этот метод может быть вызван, даже если пользователь уже вошел в учетная запись Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="270e4-114">This method may be called even if a user is already logged on to a Microsoft account.</span></span> <span data-ttu-id="270e4-115">В этом случае метод возвращает **значение true** без отображения учетная запись Майкрософт пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="270e4-115">In that case, the method returns **true** without displaying the Microsoft account log on UI.</span></span>

## <a name="requirements"></a><span data-ttu-id="270e4-116">Требования</span><span class="sxs-lookup"><span data-stu-id="270e4-116">Requirements</span></span>



| <span data-ttu-id="270e4-117">Требование</span><span class="sxs-lookup"><span data-stu-id="270e4-117">Requirement</span></span> | <span data-ttu-id="270e4-118">Значение</span><span class="sxs-lookup"><span data-stu-id="270e4-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="270e4-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="270e4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="270e4-120">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="270e4-120">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="270e4-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="270e4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="270e4-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="270e4-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="270e4-123">Header</span><span class="sxs-lookup"><span data-stu-id="270e4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="270e4-124"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="270e4-124"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="270e4-125">IDL</span><span class="sxs-lookup"><span data-stu-id="270e4-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="270e4-126"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="270e4-126"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="270e4-127">DLL</span><span class="sxs-lookup"><span data-stu-id="270e4-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="270e4-128"><dt>Shell32.dll (версия 6,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="270e4-128"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 
