---
description: Задает конкретный параметр входа Microsoft .NET Passport.
ms.assetid: 5ec79faa-1c74-42a4-b964-ea15edacda79
title: 'IPassportManager3: метод ut_Option:p'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPassportManager3.put_Option
api_type:
- COM
api_location: ''
ms.openlocfilehash: 52a1324c4b1a04a207b5bccac1a95bcd060be8ca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990363"
---
# <a name="ipassportmanager3put_option-method"></a><span data-ttu-id="82ed0-103">IPassportManager3::p \_ метод параметра UT</span><span class="sxs-lookup"><span data-stu-id="82ed0-103">IPassportManager3::put\_Option method</span></span>

<span data-ttu-id="82ed0-104">Задает конкретный параметр входа Microsoft .NET Passport.</span><span class="sxs-lookup"><span data-stu-id="82ed0-104">Sets a specific Microsoft .NET Passport sign-in option.</span></span>

> [!Note]  
> <span data-ttu-id="82ed0-105">Метод **\_ варианта размещения** принадлежит интерфейсу [**IPassportManager3**](/previous-versions/ms817681(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="82ed0-105">The **put\_Option** method belongs to the [**IPassportManager3**](/previous-versions/ms817681(v=msdn.10)) interface.</span></span> <span data-ttu-id="82ed0-106">Этот раздел дополняет исходную документацию.</span><span class="sxs-lookup"><span data-stu-id="82ed0-106">This topic supplements the initial documentation.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="82ed0-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="82ed0-107">Syntax</span></span>


```C++
HRESULT put_Option(
   BSTR    name,
   VARIANT newVal
);
```



## <a name="parameters"></a><span data-ttu-id="82ed0-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="82ed0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82ed0-109">*name*</span><span class="sxs-lookup"><span data-stu-id="82ed0-109">*name*</span></span> 
</dt> <dd>

<span data-ttu-id="82ed0-110">Параметр входа для установки.</span><span class="sxs-lookup"><span data-stu-id="82ed0-110">The sign-in option to be set.</span></span> <span data-ttu-id="82ed0-111">В настоящее время единственным поддерживаемым параметром является Имоде.</span><span class="sxs-lookup"><span data-stu-id="82ed0-111">Currently, the only supported option is iMode.</span></span>

</dd> <dt>

<span data-ttu-id="82ed0-112">*неввал*</span><span class="sxs-lookup"><span data-stu-id="82ed0-112">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="82ed0-113">**Вариант Variant** ( \_ логическое значение VT), указывающий новый параметр.</span><span class="sxs-lookup"><span data-stu-id="82ed0-113">A **VARIANT** (VT\_BOOL) that specifies the new value for the option.</span></span> <span data-ttu-id="82ed0-114">Это значение может быть true или false.</span><span class="sxs-lookup"><span data-stu-id="82ed0-114">This value can be True or False.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82ed0-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="82ed0-115">Return value</span></span>

<span data-ttu-id="82ed0-116">\_При успешном выполнении метода возвращает значение ОК.</span><span class="sxs-lookup"><span data-stu-id="82ed0-116">Returns S\_OK when the method succeeds.</span></span>

## <a name="remarks"></a><span data-ttu-id="82ed0-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="82ed0-117">Remarks</span></span>

<span data-ttu-id="82ed0-118">Этот метод поставляется со старыми версиями пакета SDK для Passport.</span><span class="sxs-lookup"><span data-stu-id="82ed0-118">This method ships with older versions of the Passport SDK.</span></span>

 

 
