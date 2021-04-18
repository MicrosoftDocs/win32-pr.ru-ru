---
title: Ивмплибрарисервицес Жеткаунтбитипе, метод
description: Метод Жеткаунтбитипе возвращает количество доступных библиотек указанного типа.
ms.assetid: 75f22e21-fbaf-45dc-b64f-1f687a3cf241
keywords:
- Жеткаунтбитипе метод Windows Media Player
- Жеткаунтбитипе метод проигрывателя Windows Media Player, интерфейс Ивмплибрарисервицес
- Интерфейс Ивмплибрарисервицес Windows Media Player, метод Жеткаунтбитипе
topic_type:
- apiref
api_name:
- IWMPLibraryServices.getCountByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efbd874c06c2557102011c63ee1abb895d092656
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669265"
---
# <a name="iwmplibraryservicesgetcountbytype-method"></a><span data-ttu-id="ebd07-106">Метод Ивмплибрарисервицес:: Жеткаунтбитипе</span><span class="sxs-lookup"><span data-stu-id="ebd07-106">IWMPLibraryServices::getCountByType method</span></span>

<span data-ttu-id="ebd07-107">Метод **жеткаунтбитипе** возвращает количество доступных библиотек указанного типа.</span><span class="sxs-lookup"><span data-stu-id="ebd07-107">The **getCountByType** method returns the count of available libraries of a specified type.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebd07-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ebd07-108">Syntax</span></span>


```CSharp
public System.Int32 getCountByType(
  WMPLibraryType wmplt
);
```


```VB

Public Function getCountByType( _
  ByVal wmplt As WMPLibraryType _
) As System.Int32
Implements IWMPLibraryServices.getCountByType
```





## <a name="parameters"></a><span data-ttu-id="ebd07-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="ebd07-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebd07-110">*вмплт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ebd07-110">*wmplt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebd07-111">Значение из перечисления **вмплиб. вмплибраритипе** , указывающее тип библиотеки для подсчета.</span><span class="sxs-lookup"><span data-stu-id="ebd07-111">A value from the **WMPLib.WMPLibraryType** enumeration that specifies the type of library to count.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebd07-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ebd07-112">Return value</span></span>

<span data-ttu-id="ebd07-113">Значение **System. Int32** , которое является счетчиком библиотеки.</span><span class="sxs-lookup"><span data-stu-id="ebd07-113">A **System.Int32** that is the library count.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebd07-114">Требования</span><span class="sxs-lookup"><span data-stu-id="ebd07-114">Requirements</span></span>



| <span data-ttu-id="ebd07-115">Требование</span><span class="sxs-lookup"><span data-stu-id="ebd07-115">Requirement</span></span> | <span data-ttu-id="ebd07-116">Значение</span><span class="sxs-lookup"><span data-stu-id="ebd07-116">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebd07-117">Версия</span><span class="sxs-lookup"><span data-stu-id="ebd07-117">Version</span></span><br/>   | <span data-ttu-id="ebd07-118">Проигрыватель Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="ebd07-118">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="ebd07-119">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ebd07-119">Namespace</span></span><br/> | <span data-ttu-id="ebd07-120">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="ebd07-120">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="ebd07-121">Сборка</span><span class="sxs-lookup"><span data-stu-id="ebd07-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="ebd07-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="ebd07-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebd07-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ebd07-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebd07-124">**Интерфейс Ивмплибрарисервицес (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="ebd07-124">**IWMPLibraryServices Interface (VB and C#)**</span></span>](iwmplibraryservices--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ebd07-125">**вмплибраритипе**</span><span class="sxs-lookup"><span data-stu-id="ebd07-125">**WMPLibraryType**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmplibrarytype)
</dt> </dl>

 

 





