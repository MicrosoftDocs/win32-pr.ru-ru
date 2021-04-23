---
description: Получает значение конкретного параметра входа Microsoft .NET Passport.
ms.assetid: a38ffed3-a45b-4bac-8101-3e09f34f3891
title: 'Метод IPassportManager3:: get_Option'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPassportManager3.get_Option
api_type:
- COM
api_location: ''
ms.openlocfilehash: 289daf9ffbaad872115d0abfd7a618a4f7e44c10
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423198"
---
# <a name="ipassportmanager3get_option-method"></a><span data-ttu-id="ea8eb-103">Метод IPassportManager3:: Get \_</span><span class="sxs-lookup"><span data-stu-id="ea8eb-103">IPassportManager3::get\_Option method</span></span>

<span data-ttu-id="ea8eb-104">Получает значение конкретного параметра входа Microsoft .NET Passport.</span><span class="sxs-lookup"><span data-stu-id="ea8eb-104">Retrieves the value of a specific Microsoft .NET Passport sign-in option.</span></span>

> [!Note]  
> <span data-ttu-id="ea8eb-105">Метод **получения \_ параметра** принадлежит интерфейсу [**IPassportManager3**](/previous-versions/ms817681(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="ea8eb-105">The **get\_Option** method belongs to the [**IPassportManager3**](/previous-versions/ms817681(v=msdn.10)) interface.</span></span> <span data-ttu-id="ea8eb-106">Этот раздел дополняет исходную документацию.</span><span class="sxs-lookup"><span data-stu-id="ea8eb-106">This topic supplements the initial documentation.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="ea8eb-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ea8eb-107">Syntax</span></span>


```C++
HRESULT get_Option(
  [in]  BSTR    name,
  [out] VARIANT *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="ea8eb-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ea8eb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea8eb-109">*имя* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ea8eb-109">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea8eb-110">Возвращаемый параметр входа.</span><span class="sxs-lookup"><span data-stu-id="ea8eb-110">The sign-in option to be retrieved.</span></span> <span data-ttu-id="ea8eb-111">В настоящее время поддерживается только параметр "Имоде".</span><span class="sxs-lookup"><span data-stu-id="ea8eb-111">Currently, the only supported option is "iMode".</span></span>

</dd> <dt>

<span data-ttu-id="ea8eb-112">*Pval* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ea8eb-112">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ea8eb-113">Указатель на **вариант Variant (тип** \_ bool), который получает значение параметра.</span><span class="sxs-lookup"><span data-stu-id="ea8eb-113">A pointer to a **VARIANT** (VT\_BOOL) that receives the value of the option.</span></span> <span data-ttu-id="ea8eb-114">Это значение может быть true или false.</span><span class="sxs-lookup"><span data-stu-id="ea8eb-114">This value can be True or False.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea8eb-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ea8eb-115">Return value</span></span>

<span data-ttu-id="ea8eb-116">\_При успешном выполнении метода возвращает значение ОК.</span><span class="sxs-lookup"><span data-stu-id="ea8eb-116">Returns S\_OK when the method succeeds.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea8eb-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ea8eb-117">Remarks</span></span>

<span data-ttu-id="ea8eb-118">Этот метод поставляется со старыми версиями пакета SDK для Passport.</span><span class="sxs-lookup"><span data-stu-id="ea8eb-118">This method ships with older versions of the Passport SDK.</span></span>

 

 
