---
title: Ивмпкдром ДривеспеЦифиер, свойство
description: Свойство ДривеспеЦифиер получает букву CD или DVD-дисковода.
ms.assetid: 8865232a-08a3-447b-a6d6-2bfda3a689e1
keywords:
- Проигрыватель Windows Media для свойства ДривеспеЦифиер
- ДривеспеЦифиер свойство проигрывателя Windows Media Player, интерфейс Ивмпкдром
- Интерфейс Ивмпкдром Windows Media Player, свойство ДривеспеЦифиер
topic_type:
- apiref
api_name:
- IWMPCdrom.driveSpecifier
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0a6c439523d90824da708700d48274f5a2e5ef4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708338"
---
# <a name="iwmpcdromdrivespecifier-property"></a><span data-ttu-id="f09d7-106">Ивмпкдром: свойство РивеспеЦифиер:d</span><span class="sxs-lookup"><span data-stu-id="f09d7-106">IWMPCdrom::driveSpecifier property</span></span>

<span data-ttu-id="f09d7-107">Свойство **дривеспеЦифиер** получает букву CD или DVD-дисковода.</span><span class="sxs-lookup"><span data-stu-id="f09d7-107">The **driveSpecifier** property gets the CD or DVD drive letter.</span></span>

## <a name="syntax"></a><span data-ttu-id="f09d7-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f09d7-108">Syntax</span></span>


```CSharp
public System.String driveSpecifier {get; set;}
```


```VB

Public ReadOnly Property driveSpecifier As System.String
```





## <a name="property-value"></a><span data-ttu-id="f09d7-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="f09d7-109">Property value</span></span>

<span data-ttu-id="f09d7-110">**Строка System. String** , которая является буквой диска.</span><span class="sxs-lookup"><span data-stu-id="f09d7-110">A **System.String** that is the drive letter.</span></span>

## <a name="remarks"></a><span data-ttu-id="f09d7-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f09d7-111">Remarks</span></span>

<span data-ttu-id="f09d7-112">Обычно дисководы DVD могут воспроизводить компакт-диски, но дисководы компакт-дисков не могут воспроизводить DVD-носители.</span><span class="sxs-lookup"><span data-stu-id="f09d7-112">Typically, DVD drives can play CD media, but CD drives cannot play DVD media.</span></span>

<span data-ttu-id="f09d7-113">Это свойство возвращает букву диска для индекса диска, начинающегося с нуля, в диапазоне, полученном с помощью **ивмпкдромколлектион. Count**.</span><span class="sxs-lookup"><span data-stu-id="f09d7-113">This property gets a drive letter for a zero-based drive index within the range retrieved using **IWMPCdromCollection.count**.</span></span> <span data-ttu-id="f09d7-114">Полученное значение имеет вид *x*:, где *X* представляет букву диска.</span><span class="sxs-lookup"><span data-stu-id="f09d7-114">The value retrieved takes the form *X*:, where *X* represents the drive letter.</span></span>

<span data-ttu-id="f09d7-115">Чтобы получить значение этого свойства, требуется доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="f09d7-115">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="f09d7-116">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="f09d7-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="f09d7-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="f09d7-117">Examples</span></span>

<span data-ttu-id="f09d7-118">В следующем примере **дривеспеЦифиер** используется для создания строки, содержащей список доступных ДИСКОВОДОВ компакт-дисков и дисков DVD, и отображает эту строку в окне сообщения.</span><span class="sxs-lookup"><span data-stu-id="f09d7-118">The following example uses **driveSpecifier** to build a string that contains a list of available CD and DVD drives and displays that string in a message box.</span></span> <span data-ttu-id="f09d7-119">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="f09d7-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// String that will contain the list of drive specifiers.
string MyDriveSpecifiers = "Drive letters found:  ";

// Store the number of available drives.
int numDrives = player.cdromCollection.count;

// Loop through the available drives. 
for (int i = 0; i < numDrives; i++)
{
    MyDriveSpecifiers += player.cdromCollection.Item(i).driveSpecifier;
    MyDriveSpecifiers += " ";
}

// Display the list of drive specifiers in a message box.
System.Windows.Forms.MessageBox.Show(MyDriveSpecifiers);
```


```VB

'  String that will contain the list of drive specifiers.
Dim MyDriveSpecifiers As String = &quot;Drive letters found:  &quot;

&#39;  Store the number of available drives.
Dim numDrives = player.cdromCollection.count

&#39;  Loop through the available drives. 
For i As Integer = 0 To (numDrives - 1)
    MyDriveSpecifiers += player.cdromCollection.Item(i).driveSpecifier
    MyDriveSpecifiers += &quot; &quot;
Next i

&#39;  Display the list of drive specifiers in a message box.
System.Windows.Forms.MessageBox.Show(MyDriveSpecifiers)
```





## <a name="requirements"></a><span data-ttu-id="f09d7-120">Требования</span><span class="sxs-lookup"><span data-stu-id="f09d7-120">Requirements</span></span>



| <span data-ttu-id="f09d7-121">Требование</span><span class="sxs-lookup"><span data-stu-id="f09d7-121">Requirement</span></span> | <span data-ttu-id="f09d7-122">Значение</span><span class="sxs-lookup"><span data-stu-id="f09d7-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f09d7-123">Версия</span><span class="sxs-lookup"><span data-stu-id="f09d7-123">Version</span></span><br/>   | <span data-ttu-id="f09d7-124">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="f09d7-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="f09d7-125">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f09d7-125">Namespace</span></span><br/> | <span data-ttu-id="f09d7-126">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="f09d7-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="f09d7-127">Сборка</span><span class="sxs-lookup"><span data-stu-id="f09d7-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f09d7-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="f09d7-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f09d7-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f09d7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f09d7-130">**Интерфейс Ивмпкдром (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="f09d7-130">**IWMPCdrom Interface (VB and C#)**</span></span>](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f09d7-131">**Ивмпкдромколлектион. Count (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="f09d7-131">**IWMPCdromCollection.count (VB and C#)**</span></span>](wmplibiwmpcdromcollection-iwmpcdromcollection-count--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f09d7-132">**IWMPSettings2. Медиаакцессригхтс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="f09d7-132">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f09d7-133">**IWMPSettings2. Рекуестмедиаакцессригхтс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="f09d7-133">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





