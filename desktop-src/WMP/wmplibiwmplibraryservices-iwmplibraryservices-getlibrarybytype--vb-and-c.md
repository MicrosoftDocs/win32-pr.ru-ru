---
title: Ивмплибрарисервицес Жетлибрарибитипе, метод
description: Метод Жетлибрарибитипе возвращает интерфейс Ивмплибрари, представляющий библиотеку с указанным типом и индексом.
ms.assetid: 2507c764-a2cf-42f9-ad44-eaf040b78891
keywords:
- Жетлибрарибитипе метод Windows Media Player
- Жетлибрарибитипе метод проигрывателя Windows Media Player, интерфейс Ивмплибрарисервицес
- Интерфейс Ивмплибрарисервицес Windows Media Player, метод Жетлибрарибитипе
topic_type:
- apiref
api_name:
- IWMPLibraryServices.getLibraryByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d57fcc71f912fe1ee896ec893ea8f556eeb2277
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669263"
---
# <a name="iwmplibraryservicesgetlibrarybytype-method"></a><span data-ttu-id="baa60-106">Метод Ивмплибрарисервицес:: Жетлибрарибитипе</span><span class="sxs-lookup"><span data-stu-id="baa60-106">IWMPLibraryServices::getLibraryByType method</span></span>

<span data-ttu-id="baa60-107">Метод **жетлибрарибитипе** возвращает интерфейс **ивмплибрари** , представляющий библиотеку с указанным типом и индексом.</span><span class="sxs-lookup"><span data-stu-id="baa60-107">The **getLibraryByType** method returns an **IWMPLibrary** interface that represents the library that has the specified type and index.</span></span>

## <a name="syntax"></a><span data-ttu-id="baa60-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="baa60-108">Syntax</span></span>


```CSharp
public IWMPLibrary getLibraryByType(
  WMPLibraryType wmplt,
  System.Int32 lIndex
);
```


```VB

Public Function getLibraryByType( _
  ByVal wmplt As WMPLibraryType, _
  ByVal lIndex As System.Int32 _
) As IWMPLibrary
Implements IWMPLibraryServices.getLibraryByType
```





## <a name="parameters"></a><span data-ttu-id="baa60-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="baa60-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="baa60-110">*вмплт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="baa60-110">*wmplt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="baa60-111">Значение из перечисления **вмплиб. вмплибраритипе** , указывающее тип извлекаемой библиотеки.</span><span class="sxs-lookup"><span data-stu-id="baa60-111">A value from the **WMPLib.WMPLibraryType** enumeration that specifies the type of library to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="baa60-112">*Линдекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="baa60-112">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="baa60-113">Объект **System. Int32** , который является индексом извлекаемой библиотеки.</span><span class="sxs-lookup"><span data-stu-id="baa60-113">A **System.Int32** that is the index of the library to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="baa60-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="baa60-114">Return value</span></span>

<span data-ttu-id="baa60-115">Интерфейс **вмплиб. ивмплибрари** для возвращаемой библиотеки.</span><span class="sxs-lookup"><span data-stu-id="baa60-115">A **WMPLib.IWMPLibrary** interface for the library that is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="baa60-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="baa60-116">Remarks</span></span>

<span data-ttu-id="baa60-117">Существует только одна локальная Библиотека, и библиотеки дисков доступны только на компакт-дисках с данными и DVD-дисках, содержащих мультимедийное содержимое.</span><span class="sxs-lookup"><span data-stu-id="baa60-117">There is only one local library, and disc libraries are available only on data CDs and DVDs that contain media content.</span></span>

## <a name="requirements"></a><span data-ttu-id="baa60-118">Требования</span><span class="sxs-lookup"><span data-stu-id="baa60-118">Requirements</span></span>



| <span data-ttu-id="baa60-119">Требование</span><span class="sxs-lookup"><span data-stu-id="baa60-119">Requirement</span></span> | <span data-ttu-id="baa60-120">Значение</span><span class="sxs-lookup"><span data-stu-id="baa60-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="baa60-121">Версия</span><span class="sxs-lookup"><span data-stu-id="baa60-121">Version</span></span><br/>   | <span data-ttu-id="baa60-122">Проигрыватель Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="baa60-122">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="baa60-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="baa60-123">Namespace</span></span><br/> | <span data-ttu-id="baa60-124">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="baa60-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="baa60-125">Сборка</span><span class="sxs-lookup"><span data-stu-id="baa60-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="baa60-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="baa60-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="baa60-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="baa60-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="baa60-128">**Интерфейс Ивмплибрари (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="baa60-128">**IWMPLibrary Interface (VB and C#)**</span></span>](iwmplibrary--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="baa60-129">**Интерфейс Ивмплибрарисервицес (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="baa60-129">**IWMPLibraryServices Interface (VB and C#)**</span></span>](iwmplibraryservices--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="baa60-130">**вмплибраритипе**</span><span class="sxs-lookup"><span data-stu-id="baa60-130">**WMPLibraryType**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmplibrarytype)
</dt> </dl>

 

 





