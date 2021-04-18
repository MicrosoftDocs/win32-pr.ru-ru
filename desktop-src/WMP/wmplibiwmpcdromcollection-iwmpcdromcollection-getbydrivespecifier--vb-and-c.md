---
title: Ивмпкдромколлектион ЖетбидривеспеЦифиер, метод
description: Метод ЖетбидривеспеЦифиер возвращает интерфейс Ивмпкдром, связанный с определенной буквой диска.
ms.assetid: 4a550eb1-a37e-43fd-9e08-801c4fd64e68
keywords:
- ЖетбидривеспеЦифиер метод Windows Media Player
- ЖетбидривеспеЦифиер метод проигрывателя Windows Media Player, интерфейс Ивмпкдромколлектион
- Интерфейс Ивмпкдромколлектион Windows Media Player, метод ЖетбидривеспеЦифиер
topic_type:
- apiref
api_name:
- IWMPCdromCollection.getByDriveSpecifier
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe771fc893d4bf43b82dc825a2d33724926e8151
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717959"
---
# <a name="iwmpcdromcollectiongetbydrivespecifier-method"></a><span data-ttu-id="9a8ee-106">Метод Ивмпкдромколлектион:: ЖетбидривеспеЦифиер</span><span class="sxs-lookup"><span data-stu-id="9a8ee-106">IWMPCdromCollection::getByDriveSpecifier method</span></span>

<span data-ttu-id="9a8ee-107">Метод **жетбидривеспеЦифиер** возвращает интерфейс **ивмпкдром** , связанный с определенной буквой диска.</span><span class="sxs-lookup"><span data-stu-id="9a8ee-107">The **getByDriveSpecifier** method returns an **IWMPCdrom** interface associated with a particular drive letter.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a8ee-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9a8ee-108">Syntax</span></span>


```CSharp
public IWMPCdrom getByDriveSpecifier(
  System.String bstrDriveSpecifier
);
```


```VB

Public Function getByDriveSpecifier( _
  ByVal bstrDriveSpecifier As System.String _
) As IWMPCdrom
Implements IWMPCdromCollection.getByDriveSpecifier
```





## <a name="parameters"></a><span data-ttu-id="9a8ee-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="9a8ee-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a8ee-110">*бстрдривеспеЦифиер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9a8ee-110">*bstrDriveSpecifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a8ee-111">**Строка System. String** , которая является буквой диска, за которой следует символ двоеточия (":").</span><span class="sxs-lookup"><span data-stu-id="9a8ee-111">A **System.String** that is the drive letter followed by a colon (":") character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a8ee-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9a8ee-112">Return value</span></span>

<span data-ttu-id="9a8ee-113">Интерфейс **вмплиб. ивмпкдром** .</span><span class="sxs-lookup"><span data-stu-id="9a8ee-113">A **WMPLib.IWMPCdrom** interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a8ee-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9a8ee-114">Remarks</span></span>

<span data-ttu-id="9a8ee-115">Буквы дисков должны быть заданы в формате *x*:, где *X* обозначает букву диска.</span><span class="sxs-lookup"><span data-stu-id="9a8ee-115">Drive letters must be given in the form *X*:, where *X* represents the drive letter.</span></span>

<span data-ttu-id="9a8ee-116">Чтобы использовать этот метод, требуется доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="9a8ee-116">To use this method, read access to the library is required.</span></span> <span data-ttu-id="9a8ee-117">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="9a8ee-117">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="9a8ee-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="9a8ee-118">Examples</span></span>

<span data-ttu-id="9a8ee-119">В следующем примере используется **жетбидривеспеЦифиер** для получения интерфейса **ивмпкдром** , соответствующего букве диска, предоставленной пользователем в текстовом поле.</span><span class="sxs-lookup"><span data-stu-id="9a8ee-119">The following example uses **getByDriveSpecifier** to get the **IWMPCdrom** interface that corresponds to a drive letter provided by the user in a text box.</span></span> <span data-ttu-id="9a8ee-120">Затем вызывается метод **ивмпкдром. EJECT** для извлечения указанного диска.</span><span class="sxs-lookup"><span data-stu-id="9a8ee-120">The **IWMPCdrom.eject** method is then called to eject the specified drive.</span></span> <span data-ttu-id="9a8ee-121">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="9a8ee-121">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Store the drive letter provided by the user.
string driveLetter = myText.Text;

// Append a colon to the drive letter to create a valid drive specifier.
driveLetter += ":";

// Get an IWMPCdrom interface for the drive.
WMPLib.IWMPCdrom drive = player.cdromCollection.getByDriveSpecifier(driveLetter);

// Use the eject method of the IWMPCdrom interface to open the drive door.
drive.eject();
```


```VB

' Store the drive letter provided by the user.
Dim driveLetter As String = myText.Text

&#39; Append a colon to the drive letter to create a valid drive specifier.
driveLetter += &quot;:&quot;

&#39; Get an IWMPCdrom interface for the drive.
Dim drive As WMPLib.IWMPCdrom = player.cdromCollection.getByDriveSpecifier(driveLetter)

&#39; Use the eject method of the IWMPCdrom interface to open the drive door.
drive.eject()
```





## <a name="requirements"></a><span data-ttu-id="9a8ee-122">Требования</span><span class="sxs-lookup"><span data-stu-id="9a8ee-122">Requirements</span></span>



| <span data-ttu-id="9a8ee-123">Требование</span><span class="sxs-lookup"><span data-stu-id="9a8ee-123">Requirement</span></span> | <span data-ttu-id="9a8ee-124">Значение</span><span class="sxs-lookup"><span data-stu-id="9a8ee-124">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a8ee-125">Версия</span><span class="sxs-lookup"><span data-stu-id="9a8ee-125">Version</span></span><br/>   | <span data-ttu-id="9a8ee-126">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="9a8ee-126">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="9a8ee-127">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9a8ee-127">Namespace</span></span><br/> | <span data-ttu-id="9a8ee-128">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="9a8ee-128">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="9a8ee-129">Сборка</span><span class="sxs-lookup"><span data-stu-id="9a8ee-129">Assembly</span></span><br/>  | <dl> <span data-ttu-id="9a8ee-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="9a8ee-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a8ee-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9a8ee-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a8ee-132">**Интерфейс Ивмпкдром (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="9a8ee-132">**IWMPCdrom Interface (VB and C#)**</span></span>](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9a8ee-133">**Ивмпкдром. EJECT (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="9a8ee-133">**IWMPCdrom.eject (VB and C#)**</span></span>](wmplibiwmpcdrom-iwmpcdrom-eject--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9a8ee-134">**Интерфейс Ивмпкдромколлектион (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="9a8ee-134">**IWMPCdromCollection Interface (VB and C#)**</span></span>](iwmpcdromcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9a8ee-135">**IWMPSettings2. Медиаакцессригхтс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="9a8ee-135">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9a8ee-136">**IWMPSettings2. Рекуестмедиаакцессригхтс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="9a8ee-136">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





