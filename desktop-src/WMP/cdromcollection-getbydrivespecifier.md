---
title: Кдромколлектион. ЖетбидривеспеЦифиер, метод
description: Метод ЖетбидривеспеЦифиер извлекает объект CDROM, связанный с определенной буквой диска.
ms.assetid: 60626ffc-3d10-435b-8827-c5d7b6e02607
keywords:
- ЖетбидривеспеЦифиер метод Windows Media Player
- ЖетбидривеспеЦифиер метод Windows Media Player, класс Кдромколлектион
- Класс Кдромколлектион Windows Media Player, метод ЖетбидривеспеЦифиер
topic_type:
- apiref
api_name:
- CdromCollection.getByDriveSpecifier
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 807b44a7be97ac93b5b0f270c2d1723404887c9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699176"
---
# <a name="cdromcollectiongetbydrivespecifier-method"></a><span data-ttu-id="8031a-106">Кдромколлектион. ЖетбидривеспеЦифиер, метод</span><span class="sxs-lookup"><span data-stu-id="8031a-106">CdromCollection.getByDriveSpecifier method</span></span>

<span data-ttu-id="8031a-107">Метод **жетбидривеспеЦифиер** извлекает объект **CDROM** , связанный с определенной буквой диска.</span><span class="sxs-lookup"><span data-stu-id="8031a-107">The **getByDriveSpecifier** method retrieves the **Cdrom** object associated with a particular drive letter.</span></span>

## <a name="syntax"></a><span data-ttu-id="8031a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8031a-108">Syntax</span></span>


```JScript
retVal = CdromCollection.getByDriveSpecifier(
  driveSpecifier
)
```



## <a name="parameters"></a><span data-ttu-id="8031a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="8031a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8031a-110">*дривеспеЦифиер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8031a-110">*driveSpecifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8031a-111">**Строка** , содержащая букву диска, за которой следует символ двоеточия (":").</span><span class="sxs-lookup"><span data-stu-id="8031a-111">**String** containing the drive letter followed by a colon (":") character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8031a-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8031a-112">Return value</span></span>

<span data-ttu-id="8031a-113">Этот метод возвращает объект **CDROM** .</span><span class="sxs-lookup"><span data-stu-id="8031a-113">This method returns a **Cdrom** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8031a-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8031a-114">Remarks</span></span>

<span data-ttu-id="8031a-115">Буквы дисков должны быть заданы в формате *x*:, где *X* обозначает букву диска.</span><span class="sxs-lookup"><span data-stu-id="8031a-115">Drive letters must be given in the form *X*:, where *X* represents the drive letter.</span></span>

<span data-ttu-id="8031a-116">Чтобы использовать этот метод, требуется доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="8031a-116">To use this method, read access to the library is required.</span></span> <span data-ttu-id="8031a-117">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="8031a-117">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="8031a-118">**Проигрыватель Windows Media 10 Mobile:** Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8031a-118">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="8031a-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="8031a-119">Examples</span></span>

<span data-ttu-id="8031a-120">В следующем примере JScript используется *кдромколлектион*. **жетбидривеспеЦифиер** получить объект **CDROM** , соответствующий букве диска, предоставленной пользователем.</span><span class="sxs-lookup"><span data-stu-id="8031a-120">The following JScript example uses *CdromCollection*.**getByDriveSpecifier** to retrieve the **Cdrom** object that corresponds to a drive letter provided by the user.</span></span> <span data-ttu-id="8031a-121">Был создан HTML-элемент text с именем NAME = "MyText" для вводимых пользователем данных.</span><span class="sxs-lookup"><span data-stu-id="8031a-121">An HTML text element was created, with NAME = "MyText", for user input.</span></span> <span data-ttu-id="8031a-122">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="8031a-122">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Store the drive letter provided by the user.
var DriveLetter = MyText.value;

// Append a colon to the drive letter to create a valid drive specifier.
DriveLetter += ":";

// Get the Cdrom object using the drive specifier.
var Drive = Player.cdRomCollection.getByDriveSpecifier(DriveLetter);

// Use the Cdrom object to open the drive door.
Drive.eject();
```



## <a name="requirements"></a><span data-ttu-id="8031a-123">Требования</span><span class="sxs-lookup"><span data-stu-id="8031a-123">Requirements</span></span>



| <span data-ttu-id="8031a-124">Требование</span><span class="sxs-lookup"><span data-stu-id="8031a-124">Requirement</span></span> | <span data-ttu-id="8031a-125">Значение</span><span class="sxs-lookup"><span data-stu-id="8031a-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8031a-126">Версия</span><span class="sxs-lookup"><span data-stu-id="8031a-126">Version</span></span><br/> | <span data-ttu-id="8031a-127">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="8031a-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="8031a-128">DLL</span><span class="sxs-lookup"><span data-stu-id="8031a-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="8031a-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8031a-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8031a-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8031a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8031a-131">**Объект CDROM**</span><span class="sxs-lookup"><span data-stu-id="8031a-131">**Cdrom Object**</span></span>](cdrom-object.md)
</dt> <dt>

[<span data-ttu-id="8031a-132">**CDROM. EJECT**</span><span class="sxs-lookup"><span data-stu-id="8031a-132">**Cdrom.eject**</span></span>](cdrom-eject.md)
</dt> <dt>

[<span data-ttu-id="8031a-133">**Объект Кдромколлектион**</span><span class="sxs-lookup"><span data-stu-id="8031a-133">**CdromCollection Object**</span></span>](cdromcollection-object.md)
</dt> <dt>

[<span data-ttu-id="8031a-134">**Settings. Медиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="8031a-134">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="8031a-135">**Settings. Рекуестмедиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="8031a-135">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





