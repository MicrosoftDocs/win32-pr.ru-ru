---
title: Кдромколлектион. ЖетбидривеспеЦифиер, метод
description: Метод ЖетбидривеспеЦифиер извлекает объект CDROM, связанный с определенной буквой диска.
ms.assetid: 60626ffc-3d10-435b-8827-c5d7b6e02607
keywords:
- проигрыватель Windows Media метода жетбидривеспеЦифиер
- проигрыватель Windows Media метода жетбидривеспеЦифиер, класс кдромколлектион
- класс кдромколлектион проигрыватель Windows Media, метод жетбидривеспеЦифиер
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
ms.openlocfilehash: fa5487b3a57fb1e7e4167561fcca08e10d6472182881fa221bd8e671bc814cc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864094"
---
# <a name="cdromcollectiongetbydrivespecifier-method"></a>Кдромколлектион. ЖетбидривеспеЦифиер, метод

Метод **жетбидривеспеЦифиер** извлекает объект **CDROM** , связанный с определенной буквой диска.

## <a name="syntax"></a>Синтаксис


```JScript
retVal = CdromCollection.getByDriveSpecifier(
  driveSpecifier
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*дривеспеЦифиер* \[ окне\]
</dt> <dd>

**Строка** , содержащая букву диска, за которой следует символ двоеточия (":").

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает объект **CDROM** .

## <a name="remarks"></a>Remarks

Буквы дисков должны быть заданы в формате *x*:, где *X* обозначает букву диска.

Чтобы использовать этот метод, требуется доступ на чтение к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

**проигрыватель Windows Media 10 Mobile:** Этот метод не поддерживается.

## <a name="examples"></a>Примеры

в следующем примере JScript используется *кдромколлектион*. **жетбидривеспеЦифиер** получить объект **CDROM** , соответствующий букве диска, предоставленной пользователем. Был создан HTML-элемент text с именем NAME = "MyText" для вводимых пользователем данных. Объект **Player** создан с идентификатором "Player".


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



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Объект CDROM**](cdrom-object.md)
</dt> <dt>

[**CDROM. EJECT**](cdrom-eject.md)
</dt> <dt>

[**Объект Кдромколлектион**](cdromcollection-object.md)
</dt> <dt>

[**Параметры. медиаакцессригхтс**](settings-mediaaccessrights.md)
</dt> <dt>

[**Параметры. рекуестмедиаакцессригхтс**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





