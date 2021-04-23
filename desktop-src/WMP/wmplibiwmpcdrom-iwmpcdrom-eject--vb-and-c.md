---
title: Метод извлечения Ивмпкдром
description: Метод Eject извлекает компакт-диск или DVD-диск из накопителя. | Метод извлечения Ивмпкдром
ms.assetid: c0a69252-fd79-452c-bc61-3c3e8bcaaf48
keywords:
- метод извлечения Windows Media Player
- метод извлечения Windows Media Player, интерфейс Ивмпкдром
- Интерфейс Ивмпкдром Windows Media Player, метод reeject
topic_type:
- apiref
api_name:
- IWMPCdrom.eject
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b8ca2403b86b648e98861d91a21db80ddb64aac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717996"
---
# <a name="iwmpcdromeject-method"></a><span data-ttu-id="a5675-107">Метод Ивмпкдром:: reeject</span><span class="sxs-lookup"><span data-stu-id="a5675-107">IWMPCdrom::eject method</span></span>

<span data-ttu-id="a5675-108">Метод **Eject** извлекает компакт-диск или DVD-диск из накопителя.</span><span class="sxs-lookup"><span data-stu-id="a5675-108">The **eject** method ejects the CD or DVD from the drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5675-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a5675-109">Syntax</span></span>


```CSharp
public void eject();
```


```VB

Public Sub eject()
Implements IWMPCdrom.eject
```





## <a name="parameters"></a><span data-ttu-id="a5675-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="a5675-110">Parameters</span></span>

<span data-ttu-id="a5675-111">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="a5675-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a5675-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a5675-112">Return value</span></span>

<span data-ttu-id="a5675-113">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="a5675-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5675-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a5675-114">Remarks</span></span>

<span data-ttu-id="a5675-115">Если дверца диска открыта, этот метод закрывает дверцу.</span><span class="sxs-lookup"><span data-stu-id="a5675-115">If the drive door is open, this method closes the door.</span></span>

<span data-ttu-id="a5675-116">Чтобы использовать этот метод, требуется доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="a5675-116">To use this method, read access to the library is required.</span></span> <span data-ttu-id="a5675-117">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="a5675-117">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a5675-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="a5675-118">Examples</span></span>

<span data-ttu-id="a5675-119">В следующем примере метод **reeject** используется для открытия дверцы компакт-диска или DVD-дисковода с нулевым индексом в ответ на событие щелчка кнопки.</span><span class="sxs-lookup"><span data-stu-id="a5675-119">The following example uses **eject** to open the door of the CD or DVD drive that has the index of zero in response to the Click event of a button.</span></span> <span data-ttu-id="a5675-120">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="a5675-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void ejectButton_Click(object o, System.EventArgs args)
{
    player.cdromCollection.Item(0).eject();
}
```


```VB

Public Sub ejectButton_Click(ByVal o As Object, ByVal args As System.EventArgs) Handles ejectButton.Click

    player.cdromCollection.Item(0).eject()

End Sub
```





## <a name="requirements"></a><span data-ttu-id="a5675-121">Требования</span><span class="sxs-lookup"><span data-stu-id="a5675-121">Requirements</span></span>



| <span data-ttu-id="a5675-122">Требование</span><span class="sxs-lookup"><span data-stu-id="a5675-122">Requirement</span></span> | <span data-ttu-id="a5675-123">Значение</span><span class="sxs-lookup"><span data-stu-id="a5675-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5675-124">Версия</span><span class="sxs-lookup"><span data-stu-id="a5675-124">Version</span></span><br/>   | <span data-ttu-id="a5675-125">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="a5675-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="a5675-126">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a5675-126">Namespace</span></span><br/> | <span data-ttu-id="a5675-127">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="a5675-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="a5675-128">Сборка</span><span class="sxs-lookup"><span data-stu-id="a5675-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a5675-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="a5675-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5675-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a5675-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5675-131">**Аксвиндовсмедиаплайер. Плайстате (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="a5675-131">**AxWindowsMediaPlayer.playState (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-playstate--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a5675-132">**Интерфейс Ивмпкдром (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="a5675-132">**IWMPCdrom Interface (VB and C#)**</span></span>](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a5675-133">**IWMPSettings2. Медиаакцессригхтс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="a5675-133">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a5675-134">**IWMPSettings2. Рекуестмедиаакцессригхтс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="a5675-134">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





