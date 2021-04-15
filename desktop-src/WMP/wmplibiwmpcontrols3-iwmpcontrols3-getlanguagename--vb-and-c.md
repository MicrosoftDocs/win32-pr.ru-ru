---
title: IWMPControls3 Жетлангуаженаме, метод
description: Метод Жетлангуаженаме возвращает имя звукового языка с указанным кодом локали (LCID).
ms.assetid: a0651e8d-0ba1-4fff-93f0-fe097231723e
keywords:
- Жетлангуаженаме метод Windows Media Player
- Жетлангуаженаме метод проигрывателя Windows Media Player, интерфейс IWMPControls3
- Интерфейс IWMPControls3 Windows Media Player, метод Жетлангуаженаме
topic_type:
- apiref
api_name:
- IWMPControls3.getLanguageName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d93bf97c7b5213e3d196897de1c3ebcfa6e6d2c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649051"
---
# <a name="iwmpcontrols3getlanguagename-method"></a>Метод IWMPControls3:: Жетлангуаженаме

Метод **жетлангуаженаме** возвращает имя звукового языка с указанным кодом локали (LCID).

## <a name="syntax"></a>Синтаксис


```CSharp
public System.String getLanguageName(
  System.Int32 lLangID
);
```


```VB

Public Function getLanguageName( _
  ByVal lLangID As System.Int32 _
) As System.String
Implements IWMPControls3.getLanguageName
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*ллангид* \[ окне\]
</dt> <dd>

Значение **System. Int32** , которое является LCID.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

**Строка System. String** , которая является именем звукового языка.

## <a name="remarks"></a>Комментарии

Код языка (LCID) однозначно определяет определенный диалект языка, который называется локальным языком.

Для содержимого на основе Windows Media свойства и методы, связанные с выбором языка, поддерживают только один выход.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | Проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс IWMPControls3 (VB и C#)**](iwmpcontrols3--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. Аудиолангуажекаунт (VB и C#)**](wmplibiwmpcontrols3-iwmpcontrols3-audiolanguagecount--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. Куррентаудиолангуаже (VB и C#)**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. Куррентаудиолангуажеиндекс (VB и C#)**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. Жетаудиолангуажедескриптион (VB и C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. Жетаудиолангуажеид (VB и C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> </dl>

 

 





