---
title: Ивмплибрари, метод тождественности
description: Метод «идентичен» возвращает значение, указывающее, совпадает ли указанный объект с текущим.
ms.assetid: c4eebc46-6a5f-4f9a-8cd4-7421b156670c
keywords:
- метод, аналогичный проигрывателю Windows Media
- тождественный метод Windows Media Player, интерфейс Ивмплибрари
- Интерфейс Ивмплибрари Windows Media Player, метод, идентичный
topic_type:
- apiref
api_name:
- IWMPLibrary.isIdentical
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53071caa98b8f8e3ccb95e926969926cc68e7860
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708527"
---
# <a name="iwmplibraryisidentical-method"></a><span data-ttu-id="a5960-106">Метод Ивмплибрари:: одинаковы</span><span class="sxs-lookup"><span data-stu-id="a5960-106">IWMPLibrary::isIdentical method</span></span>

<span data-ttu-id="a5960-107">Метод « **идентичен** » возвращает значение, указывающее, совпадает ли указанный объект с текущим.</span><span class="sxs-lookup"><span data-stu-id="a5960-107">The **isIdentical** method returns a value that indicates whether the supplied object is the same as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5960-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a5960-108">Syntax</span></span>


```CSharp
public System.Boolean isIdentical(
  IWMPLibrary pIWMPLibrary
);
```


```VB

Public Function isIdentical( _
  ByVal pIWMPLibrary As IWMPLibrary _
) As System.Boolean
Implements IWMPLibrary.isIdentical
```





## <a name="parameters"></a><span data-ttu-id="a5960-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a5960-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5960-110">*пивмплибрари* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a5960-110">*pIWMPLibrary* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5960-111">Интерфейс **вмплиб. ивмплибрари** , представляющий объект для сравнения с текущим объектом.</span><span class="sxs-lookup"><span data-stu-id="a5960-111">A **WMPLib.IWMPLibrary** interface that represents the object to compare with current one.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5960-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a5960-112">Return value</span></span>

<span data-ttu-id="a5960-113">Значение **System. Boolean** , которое является результатом сравнения.</span><span class="sxs-lookup"><span data-stu-id="a5960-113">A **System.Boolean** that is the result of the comparison.</span></span> <span data-ttu-id="a5960-114">Значение **true** указывает, что объекты одинаковы.</span><span class="sxs-lookup"><span data-stu-id="a5960-114">The value **true** indicates that the objects are the same.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5960-115">Требования</span><span class="sxs-lookup"><span data-stu-id="a5960-115">Requirements</span></span>



| <span data-ttu-id="a5960-116">Требование</span><span class="sxs-lookup"><span data-stu-id="a5960-116">Requirement</span></span> | <span data-ttu-id="a5960-117">Значение</span><span class="sxs-lookup"><span data-stu-id="a5960-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5960-118">Версия</span><span class="sxs-lookup"><span data-stu-id="a5960-118">Version</span></span><br/>   | <span data-ttu-id="a5960-119">Проигрыватель Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="a5960-119">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="a5960-120">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a5960-120">Namespace</span></span><br/> | <span data-ttu-id="a5960-121">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="a5960-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="a5960-122">Сборка</span><span class="sxs-lookup"><span data-stu-id="a5960-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a5960-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="a5960-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5960-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a5960-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5960-125">**Интерфейс Ивмплибрари (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="a5960-125">**IWMPLibrary Interface (VB and C#)**</span></span>](iwmplibrary--vb-and-c.md)
</dt> </dl>

 

 





