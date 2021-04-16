---
description: Создает объект перечислителя и передает обратно указатель на его интерфейс IEnumWiaItem2 для папок с элементами в дереве IWiaItem2 устройства Windows Image (WIA) 2,0.
ms.assetid: 0862bb6f-0464-491a-8cad-60b92d9609f1
title: 'Метод IWiaItem2:: Енумчилдитемс (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.EnumChildItems
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2de76d9bf43d10e08e5a85cd2a32d6b377680d18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497553"
---
# <a name="iwiaitem2enumchilditems-method"></a><span data-ttu-id="aca1d-103">Метод IWiaItem2:: Енумчилдитемс</span><span class="sxs-lookup"><span data-stu-id="aca1d-103">IWiaItem2::EnumChildItems method</span></span>

<span data-ttu-id="aca1d-104">Создает объект перечислителя и передает обратно указатель на его интерфейс [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) для папок с элементами в дереве [**IWiaItem2**](-wia-iwiaitem2.md) устройства Windows Image (WIA) 2,0.</span><span class="sxs-lookup"><span data-stu-id="aca1d-104">Creates an enumerator object and passes back a pointer to its [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) interface for folders with items in the [**IWiaItem2**](-wia-iwiaitem2.md) tree of a Windows Image Acquisition (WIA) 2.0 device.</span></span>

## <a name="syntax"></a><span data-ttu-id="aca1d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aca1d-105">Syntax</span></span>


```C++
HRESULT EnumChildItems(
  [in]  const GUID          *pCategoryGUID,
  [out]       IEnumWiaItem2 **ppIEnumWiaItem2
);
```



## <a name="parameters"></a><span data-ttu-id="aca1d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="aca1d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aca1d-107">*пкатегоригуид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="aca1d-107">*pCategoryGUID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aca1d-108">Тип: \**константа \* GUID* _</span><span class="sxs-lookup"><span data-stu-id="aca1d-108">Type: \**const GUID\** _</span></span>

<span data-ttu-id="aca1d-109">Указывает указатель на категорию, для которой перечисляются дочерние узлы.</span><span class="sxs-lookup"><span data-stu-id="aca1d-109">Specifies a pointer to a category for which child nodes are enumerated.</span></span> <span data-ttu-id="aca1d-110">Если значение _ \* NULL \* \*, то перечисляются все дочерние узлы.</span><span class="sxs-lookup"><span data-stu-id="aca1d-110">If _\*NULL\*\*, then all child nodes are enumerated.</span></span>

</dd> <dt>

<span data-ttu-id="aca1d-111">*ppIEnumWiaItem2* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="aca1d-111">*ppIEnumWiaItem2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aca1d-112">Тип: **[ **IEnumWiaItem2**](-wia-ienumwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="aca1d-112">Type: **[**IEnumWiaItem2**](-wia-ienumwiaitem2.md)\*\***</span></span>

<span data-ttu-id="aca1d-113">Получает адрес указателя на интерфейс [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) , создаваемый этим методом.</span><span class="sxs-lookup"><span data-stu-id="aca1d-113">Receives the address of a pointer to the [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) interface that this method creates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aca1d-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="aca1d-114">Return value</span></span>

<span data-ttu-id="aca1d-115">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="aca1d-115">Type: **HRESULT**</span></span>

<span data-ttu-id="aca1d-116">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="aca1d-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="aca1d-117">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="aca1d-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="aca1d-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="aca1d-118">Remarks</span></span>

<span data-ttu-id="aca1d-119">Система времени выполнения WIA 2,0 представляет каждое аппаратное устройство WIA 2,0 как иерархическое дерево объектов [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="aca1d-119">The WIA 2.0 run-time system represents each WIA 2.0 hardware device as a hierarchical tree of [**IWiaItem2**](-wia-iwiaitem2.md) objects.</span></span> <span data-ttu-id="aca1d-120">Метод **IWiaItem2:: енумчилдитемс** позволяет приложениям перечислять дочерние элементы в текущем элементе.</span><span class="sxs-lookup"><span data-stu-id="aca1d-120">The **IWiaItem2::EnumChildItems** method enables applications to enumerate child items in the current item.</span></span> <span data-ttu-id="aca1d-121">Однако его можно применить только к элементам, которые являются папками.</span><span class="sxs-lookup"><span data-stu-id="aca1d-121">However, it can only be applied to items that are folders.</span></span>

<span data-ttu-id="aca1d-122">Если папка не пуста, она содержит поддерево объектов [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="aca1d-122">If the folder is not empty, it contains a subtree of [**IWiaItem2**](-wia-iwiaitem2.md) objects.</span></span> <span data-ttu-id="aca1d-123">Метод **IWiaItem2:: енумчилдитемс** перечисляет все элементы, содержащиеся в папке.</span><span class="sxs-lookup"><span data-stu-id="aca1d-123">The **IWiaItem2::EnumChildItems** method enumerates all of the items contained in the folder.</span></span> <span data-ttu-id="aca1d-124">Он сохраняет указатель на перечислитель в параметре *ppIEnumWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="aca1d-124">It stores a pointer to an enumerator in the *ppIEnumWiaItem2* parameter.</span></span> <span data-ttu-id="aca1d-125">Приложения используют указатель перечислителя для выполнения перечисления дочерних элементов объекта.</span><span class="sxs-lookup"><span data-stu-id="aca1d-125">Applications use the enumerator pointer to perform the enumeration of an object's child items.</span></span>

<span data-ttu-id="aca1d-126">Приложения должны вызывать метод [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) для указателей интерфейса, которые они получают с помощью параметра *ppIEnumWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="aca1d-126">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIEnumWiaItem2* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="aca1d-127">Требования</span><span class="sxs-lookup"><span data-stu-id="aca1d-127">Requirements</span></span>



| <span data-ttu-id="aca1d-128">Требование</span><span class="sxs-lookup"><span data-stu-id="aca1d-128">Requirement</span></span> | <span data-ttu-id="aca1d-129">Значение</span><span class="sxs-lookup"><span data-stu-id="aca1d-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="aca1d-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="aca1d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="aca1d-131">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="aca1d-131">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="aca1d-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="aca1d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="aca1d-133">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="aca1d-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="aca1d-134">Header</span><span class="sxs-lookup"><span data-stu-id="aca1d-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="aca1d-135"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="aca1d-135"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="aca1d-136">IDL</span><span class="sxs-lookup"><span data-stu-id="aca1d-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="aca1d-137"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="aca1d-137"><dt>Wia.idl</dt></span></span> </dl> |



 

 
