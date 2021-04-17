---
title: Ивмпкдромколлектион Count, свойство
description: Свойство Count получает количество доступных компакт-дисков и DVD-дисководов в системе.
ms.assetid: 1359ab7e-fbe3-461c-801b-7c986f6e5687
keywords:
- Свойство Count проигрывателя Windows Media Player
- Свойство Count проигрывателя Windows Media Player, интерфейс Ивмпкдромколлектион
- Интерфейс Ивмпкдромколлектион Windows Media Player, свойство Count
topic_type:
- apiref
api_name:
- IWMPCdromCollection.count
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2da4d4d443c730d19c791a486fed4be0241b8c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717974"
---
# <a name="iwmpcdromcollectioncount-property"></a><span data-ttu-id="b73bb-106">Свойство Ивмпкдромколлектион:: count</span><span class="sxs-lookup"><span data-stu-id="b73bb-106">IWMPCdromCollection::count property</span></span>

<span data-ttu-id="b73bb-107">Свойство **Count** получает количество доступных компакт-дисков и DVD-дисководов в системе.</span><span class="sxs-lookup"><span data-stu-id="b73bb-107">The **count** property gets the number of available CD and DVD drives on the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="b73bb-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b73bb-108">Syntax</span></span>


```CSharp
public System.Int32 count {get; set;}
```


```VB

Public ReadOnly Property count As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="b73bb-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="b73bb-109">Property value</span></span>

<span data-ttu-id="b73bb-110">Значение **System. Int32** , которое является счетчиком доступных дисков.</span><span class="sxs-lookup"><span data-stu-id="b73bb-110">A **System.Int32** that is the count of available drives.</span></span>

## <a name="remarks"></a><span data-ttu-id="b73bb-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b73bb-111">Remarks</span></span>

<span data-ttu-id="b73bb-112">Чтобы получить значение этого свойства, требуется доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="b73bb-112">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="b73bb-113">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="b73bb-113">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="b73bb-114">Диски DVD подсчитываются точно так же, как и дисководы компакт-дисков.</span><span class="sxs-lookup"><span data-stu-id="b73bb-114">DVD drives are counted exactly like CD drives.</span></span> <span data-ttu-id="b73bb-115">Однако элемент управления ActiveX проигрывателя Windows Media поддерживает только функции DVD для Windows XP и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="b73bb-115">However, the Windows Media Player ActiveX control only supports DVD functionality for Windows XP or later.</span></span> <span data-ttu-id="b73bb-116">Обычно дисководы DVD могут воспроизводить компакт-диски, но дисководы компакт-дисков не могут воспроизводить DVD-носители.</span><span class="sxs-lookup"><span data-stu-id="b73bb-116">Typically, DVD drives can play CD media, but CD drives cannot play DVD media.</span></span>

## <a name="examples"></a><span data-ttu-id="b73bb-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="b73bb-117">Examples</span></span>

<span data-ttu-id="b73bb-118">В следующем примере функция Count используется для вывода в окне сообщения числа доступных дисководов компакт-дисков и DVD.</span><span class="sxs-lookup"><span data-stu-id="b73bb-118">The following example uses count to display the number of available CD and DVD drives in a message box.</span></span> <span data-ttu-id="b73bb-119">Объект Аксвмплиб. Аксвиндовсмедиаплайер представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="b73bb-119">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Store the number of available drives.
int numDrives = player.cdromCollection.count;

// Display the number of drives as a string.
System.Windows.Forms.MessageBox.Show("Number of available CD and DVD drives:  " + numDrives.ToString());
```


```VB

' Store the number of available drives.
Dim numDrives As Integer = player.cdromCollection.count

&#39; Display the number of drives as a string.
System.Windows.Forms.MessageBox.Show(&quot;Number of available CD and DVD drives:  &quot; + numDrives.ToString())
```





## <a name="requirements"></a><span data-ttu-id="b73bb-120">Требования</span><span class="sxs-lookup"><span data-stu-id="b73bb-120">Requirements</span></span>



| <span data-ttu-id="b73bb-121">Требование</span><span class="sxs-lookup"><span data-stu-id="b73bb-121">Requirement</span></span> | <span data-ttu-id="b73bb-122">Значение</span><span class="sxs-lookup"><span data-stu-id="b73bb-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b73bb-123">Версия</span><span class="sxs-lookup"><span data-stu-id="b73bb-123">Version</span></span><br/>   | <span data-ttu-id="b73bb-124">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="b73bb-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="b73bb-125">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b73bb-125">Namespace</span></span><br/> | <span data-ttu-id="b73bb-126">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="b73bb-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="b73bb-127">Сборка</span><span class="sxs-lookup"><span data-stu-id="b73bb-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b73bb-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="b73bb-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b73bb-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b73bb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b73bb-130">**Интерфейс Ивмпкдромколлектион (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="b73bb-130">**IWMPCdromCollection Interface (VB and C#)**</span></span>](iwmpcdromcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b73bb-131">**IWMPSettings2. Медиаакцессригхтс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="b73bb-131">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b73bb-132">**IWMPSettings2. Рекуестмедиаакцессригхтс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="b73bb-132">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





