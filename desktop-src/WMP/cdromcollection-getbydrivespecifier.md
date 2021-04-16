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

## <a name="remarks"></a>Комментарии

Буквы дисков должны быть заданы в формате *x*:, где *X* обозначает букву диска.

Чтобы использовать этот метод, требуется доступ на чтение к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

**Проигрыватель Windows Media 10 Mobile:** Этот метод не поддерживается.

## <a name="examples"></a>Примеры

В следующем примере JScript используется *кдромколлектион*. **жетбидривеспеЦифиер** получить объект **CDROM** , соответствующий букве диска, предоставленной пользователем. Был создан HTML-элемент text с именем NAME = "MyText" для вводимых пользователем данных. Объект **Player** создан с идентификатором "Player".


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



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект CDROM**](cdrom-object.md)
</dt> <dt>

[**CDROM. EJECT**](cdrom-eject.md)
</dt> <dt>

[**Объект Кдромколлектион**](cdromcollection-object.md)
</dt> <dt>

[**Settings. Медиаакцессригхтс**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. Рекуестмедиаакцессригхтс**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





