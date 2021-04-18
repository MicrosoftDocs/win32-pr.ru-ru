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
# <a name="iwmpcdromcollectiongetbydrivespecifier-method"></a>Метод Ивмпкдромколлектион:: ЖетбидривеспеЦифиер

Метод **жетбидривеспеЦифиер** возвращает интерфейс **ивмпкдром** , связанный с определенной буквой диска.

## <a name="syntax"></a>Синтаксис


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





## <a name="parameters"></a>Параметры

<dl> <dt>

*бстрдривеспеЦифиер* \[ окне\]
</dt> <dd>

**Строка System. String** , которая является буквой диска, за которой следует символ двоеточия (":").

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Интерфейс **вмплиб. ивмпкдром** .

## <a name="remarks"></a>Комментарии

Буквы дисков должны быть заданы в формате *x*:, где *X* обозначает букву диска.

Чтобы использовать этот метод, требуется доступ на чтение к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

## <a name="examples"></a>Примеры

В следующем примере используется **жетбидривеспеЦифиер** для получения интерфейса **ивмпкдром** , соответствующего букве диска, предоставленной пользователем в текстовом поле. Затем вызывается метод **ивмпкдром. EJECT** для извлечения указанного диска. Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.


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





## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | Проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ивмпкдром (VB и C#)**](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[**Ивмпкдром. EJECT (VB и C#)**](wmplibiwmpcdrom-iwmpcdrom-eject--vb-and-c.md)
</dt> <dt>

[**Интерфейс Ивмпкдромколлектион (VB и C#)**](iwmpcdromcollection--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. Медиаакцессригхтс (VB и C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. Рекуестмедиаакцессригхтс (VB и C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





