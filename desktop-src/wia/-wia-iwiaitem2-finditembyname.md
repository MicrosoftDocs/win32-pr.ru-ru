---
description: Выполняет поиск в дереве элементов подэлементов, используя имя в качестве ключа поиска.
ms.assetid: e4ce0bfb-9793-4928-b454-66ae1455b7b5
title: 'Метод IWiaItem2:: Финдитембинаме (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.FindItemByName
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 821be7e4abd8d1396befa886093aa197bcdea7f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711098"
---
# <a name="iwiaitem2finditembyname-method"></a><span data-ttu-id="7dd05-103">Метод IWiaItem2:: Финдитембинаме</span><span class="sxs-lookup"><span data-stu-id="7dd05-103">IWiaItem2::FindItemByName method</span></span>

<span data-ttu-id="7dd05-104">Выполняет поиск в дереве элементов подэлементов, используя имя в качестве ключа поиска.</span><span class="sxs-lookup"><span data-stu-id="7dd05-104">Searches an item's tree of subitems using the name as the search key.</span></span>

## <a name="syntax"></a><span data-ttu-id="7dd05-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7dd05-105">Syntax</span></span>


```C++
HRESULT FindItemByName(
  [in]  LONG      lFlags,
  [in]  BSTR      bstrFullItemName,
  [out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a><span data-ttu-id="7dd05-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7dd05-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7dd05-107">*лфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7dd05-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7dd05-108">Тип: **Long**</span><span class="sxs-lookup"><span data-stu-id="7dd05-108">Type: **LONG**</span></span>

<span data-ttu-id="7dd05-109">В настоящее время не используется.</span><span class="sxs-lookup"><span data-stu-id="7dd05-109">Currently unused.</span></span> <span data-ttu-id="7dd05-110">Значение должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="7dd05-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="7dd05-111">*бстрфуллитемнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7dd05-111">*bstrFullItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7dd05-112">Тип: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="7dd05-112">Type: **BSTR**</span></span>

<span data-ttu-id="7dd05-113">Указывает имя искомого элемента.</span><span class="sxs-lookup"><span data-stu-id="7dd05-113">Specifies the name fo the item to search for.</span></span>

</dd> <dt>

<span data-ttu-id="7dd05-114">*ppIWiaItem2* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7dd05-114">*ppIWiaItem2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7dd05-115">Тип: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="7dd05-115">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="7dd05-116">Получает адрес указателя на интерфейс [**IWiaItem2**](-wia-iwiaitem2.md) найденного элемента.</span><span class="sxs-lookup"><span data-stu-id="7dd05-116">Receives the address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) interface of the item found.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7dd05-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7dd05-117">Return value</span></span>

<span data-ttu-id="7dd05-118">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="7dd05-118">Type: **HRESULT**</span></span>

<span data-ttu-id="7dd05-119">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="7dd05-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7dd05-120">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7dd05-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7dd05-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7dd05-121">Remarks</span></span>

<span data-ttu-id="7dd05-122">Этот метод выполняет поиск в дереве элементов текущего элемента, используя имя в качестве ключа поиска.</span><span class="sxs-lookup"><span data-stu-id="7dd05-122">This method searches the current item's tree of sub-items using the name as the search key.</span></span> <span data-ttu-id="7dd05-123">Если **IWiaItem2:: финдитембинаме** находит элемент, указанный в *бстрфуллитемнаме*, он сохраняет адрес указателя на интерфейс [**IWiaItem2**](-wia-iwiaitem2.md) элемента в параметре *ppIWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="7dd05-123">If **IWiaItem2::FindItemByName** finds the item specified by *bstrFullItemName*, it stores the address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) interface of the item in the *ppIWiaItem2* parameter.</span></span>

<span data-ttu-id="7dd05-124">Приложения должны вызывать метод [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) для указателей интерфейса, которые они получают с помощью параметра *ppIWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="7dd05-124">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIWiaItem2* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="7dd05-125">Требования</span><span class="sxs-lookup"><span data-stu-id="7dd05-125">Requirements</span></span>



| <span data-ttu-id="7dd05-126">Требование</span><span class="sxs-lookup"><span data-stu-id="7dd05-126">Requirement</span></span> | <span data-ttu-id="7dd05-127">Значение</span><span class="sxs-lookup"><span data-stu-id="7dd05-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7dd05-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7dd05-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7dd05-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7dd05-129">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="7dd05-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7dd05-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7dd05-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7dd05-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="7dd05-132">Header</span><span class="sxs-lookup"><span data-stu-id="7dd05-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="7dd05-133"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="7dd05-133"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="7dd05-134">IDL</span><span class="sxs-lookup"><span data-stu-id="7dd05-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7dd05-135"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7dd05-135"><dt>Wia.idl</dt></span></span> </dl> |



 

 
