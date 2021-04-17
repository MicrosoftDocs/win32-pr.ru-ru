---
title: IWMPStringCollection2, метод тождественности
description: Метод «идентичен» возвращает значение, указывающее, совпадает ли объект, представленный предоставленным интерфейсом, с текущим.
ms.assetid: 826e7fd8-88f8-4a2a-9ca0-82a500099272
keywords:
- метод, аналогичный проигрывателю Windows Media
- тождественный метод Windows Media Player, интерфейс IWMPStringCollection2
- Интерфейс IWMPStringCollection2 Windows Media Player, метод, идентичный
topic_type:
- apiref
api_name:
- IWMPStringCollection2.isIdentical
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bb760dae213f28d44fbc707b4430cb151cfe578
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708465"
---
# <a name="iwmpstringcollection2isidentical-method"></a><span data-ttu-id="54b7b-106">Метод IWMPStringCollection2:: одинаковы</span><span class="sxs-lookup"><span data-stu-id="54b7b-106">IWMPStringCollection2::isIdentical method</span></span>

<span data-ttu-id="54b7b-107">Метод « **идентичен** » возвращает значение, указывающее, совпадает ли объект, представленный предоставленным интерфейсом, с текущим.</span><span class="sxs-lookup"><span data-stu-id="54b7b-107">The **isIdentical** method returns a value indicating whether the object represented by the supplied interface is the same as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="54b7b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="54b7b-108">Syntax</span></span>


```CSharp
public System.Boolean isIdentical(
  IWMPStringCollection2 pIWMPStringCollection2
);
```


```VB

Public Function isIdentical( _
  ByVal pIWMPStringCollection2 As IWMPStringCollection2 _
) As System.Boolean
Implements IWMPStringCollection2.isIdentical
```





## <a name="parameters"></a><span data-ttu-id="54b7b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="54b7b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54b7b-110">*pIWMPStringCollection2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="54b7b-110">*pIWMPStringCollection2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54b7b-111">Интерфейс **вмплиб. IWMPStringCollection2** , представляющий объект для сравнения с текущим объектом.</span><span class="sxs-lookup"><span data-stu-id="54b7b-111">The **WMPLib.IWMPStringCollection2** interface that represents the object to compare with current one.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54b7b-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="54b7b-112">Return value</span></span>

<span data-ttu-id="54b7b-113">Значение **System. Boolean** , которое является результатом сравнения.</span><span class="sxs-lookup"><span data-stu-id="54b7b-113">The **System.Boolean** that is the result of the comparison.</span></span> <span data-ttu-id="54b7b-114">Значение **true** указывает, что объекты коллекции строк одинаковы.</span><span class="sxs-lookup"><span data-stu-id="54b7b-114">A value of **true** indicates that the string collection objects are the same.</span></span>

## <a name="remarks"></a><span data-ttu-id="54b7b-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="54b7b-115">Remarks</span></span>

<span data-ttu-id="54b7b-116">Чтобы использовать этот метод, требуется доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="54b7b-116">To use this method, read access to the library is required.</span></span> <span data-ttu-id="54b7b-117">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="54b7b-117">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="54b7b-118">Требования</span><span class="sxs-lookup"><span data-stu-id="54b7b-118">Requirements</span></span>



| <span data-ttu-id="54b7b-119">Требование</span><span class="sxs-lookup"><span data-stu-id="54b7b-119">Requirement</span></span> | <span data-ttu-id="54b7b-120">Значение</span><span class="sxs-lookup"><span data-stu-id="54b7b-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54b7b-121">Версия</span><span class="sxs-lookup"><span data-stu-id="54b7b-121">Version</span></span><br/>   | <span data-ttu-id="54b7b-122">Проигрыватель Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="54b7b-122">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="54b7b-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="54b7b-123">Namespace</span></span><br/> | <span data-ttu-id="54b7b-124">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="54b7b-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="54b7b-125">Сборка</span><span class="sxs-lookup"><span data-stu-id="54b7b-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="54b7b-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="54b7b-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54b7b-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="54b7b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54b7b-128">**Интерфейс IWMPStringCollection2 (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="54b7b-128">**IWMPStringCollection2 Interface (VB and C#)**</span></span>](iwmpstringcollection2--vb-and-c.md)
</dt> </dl>

 

 





