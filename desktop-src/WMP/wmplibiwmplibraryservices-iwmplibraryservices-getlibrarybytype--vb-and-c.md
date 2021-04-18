---
title: Ивмплибрарисервицес Жетлибрарибитипе, метод
description: Метод Жетлибрарибитипе возвращает интерфейс Ивмплибрари, представляющий библиотеку с указанным типом и индексом.
ms.assetid: 2507c764-a2cf-42f9-ad44-eaf040b78891
keywords:
- Жетлибрарибитипе метод Windows Media Player
- Жетлибрарибитипе метод проигрывателя Windows Media Player, интерфейс Ивмплибрарисервицес
- Интерфейс Ивмплибрарисервицес Windows Media Player, метод Жетлибрарибитипе
topic_type:
- apiref
api_name:
- IWMPLibraryServices.getLibraryByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d57fcc71f912fe1ee896ec893ea8f556eeb2277
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669263"
---
# <a name="iwmplibraryservicesgetlibrarybytype-method"></a>Метод Ивмплибрарисервицес:: Жетлибрарибитипе

Метод **жетлибрарибитипе** возвращает интерфейс **ивмплибрари** , представляющий библиотеку с указанным типом и индексом.

## <a name="syntax"></a>Синтаксис


```CSharp
public IWMPLibrary getLibraryByType(
  WMPLibraryType wmplt,
  System.Int32 lIndex
);
```


```VB

Public Function getLibraryByType( _
  ByVal wmplt As WMPLibraryType, _
  ByVal lIndex As System.Int32 _
) As IWMPLibrary
Implements IWMPLibraryServices.getLibraryByType
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*вмплт* \[ окне\]
</dt> <dd>

Значение из перечисления **вмплиб. вмплибраритипе** , указывающее тип извлекаемой библиотеки.

</dd> <dt>

*Линдекс* \[ окне\]
</dt> <dd>

Объект **System. Int32** , который является индексом извлекаемой библиотеки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Интерфейс **вмплиб. ивмплибрари** для возвращаемой библиотеки.

## <a name="remarks"></a>Комментарии

Существует только одна локальная Библиотека, и библиотеки дисков доступны только на компакт-дисках с данными и DVD-дисках, содержащих мультимедийное содержимое.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | Проигрыватель Windows Media 11.<br/>                                                                                    |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ивмплибрари (VB и C#)**](iwmplibrary--vb-and-c.md)
</dt> <dt>

[**Интерфейс Ивмплибрарисервицес (VB и C#)**](iwmplibraryservices--vb-and-c.md)
</dt> <dt>

[**вмплибраритипе**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmplibrarytype)
</dt> </dl>

 

 





