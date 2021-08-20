---
title: IWMPControls3 Жетаудиолангуажедескриптион, метод
description: Метод Жетаудиолангуажедескриптион Возвращает описание для аудио-языка, соответствующего указанному индексу, основанному на единице.
ms.assetid: bf3db27f-ba14-409e-8942-fe863d6f3670
keywords:
- проигрыватель Windows Media метода жетаудиолангуажедескриптион
- проигрыватель Windows Media метода жетаудиолангуажедескриптион, интерфейс IWMPControls3
- проигрыватель Windows Media интерфейса IWMPControls3, метод жетаудиолангуажедескриптион
topic_type:
- apiref
api_name:
- IWMPControls3.getAudioLanguageDescription
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1172fd119671a8452ac581d3c3a27efd890456cec98f1ef8d6e61340a54c4404
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861874"
---
# <a name="iwmpcontrols3getaudiolanguagedescription-method"></a>Метод IWMPControls3:: Жетаудиолангуажедескриптион

Метод **жетаудиолангуажедескриптион** Возвращает описание для аудио-языка, соответствующего указанному индексу, основанному на единице.

## <a name="syntax"></a>Синтаксис


```CSharp
public System.String getAudioLanguageDescription(
  System.Int32 lIndex
);
```


```VB

Public Function getAudioLanguageDescription( _
  ByVal lIndex As System.Int32 _
) As System.String
Implements IWMPControls3.getAudioLanguageDescription
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*Линдекс* \[ окне\]
</dt> <dd>

Объект **System. Int32** , который является индексом звукового языка на основе одного.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

**Строка System. String** , которая является описанием звукового языка.

## <a name="remarks"></a>Remarks

для Windows содержимого на основе мультимедиа свойства и методы, связанные с выбором языка, поддерживают только один выход.

Используйте свойство **аудиолангуажекаунт** , чтобы получить количество поддерживаемых аудио языков, а затем получите доступ к звуковому языку по отдельности с помощью индекса, основанного на единицах.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс IWMPControls3 (VB и C#)**](iwmpcontrols3--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. Аудиолангуажекаунт (VB и C#)**](wmplibiwmpcontrols3-iwmpcontrols3-audiolanguagecount--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. Куррентаудиолангуажеиндекс (VB и C#)**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. Куррентаудиолангуаже (VB и C#)**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. Жетаудиолангуажеид (VB и C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. Жетлангуаженаме (VB и C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 





