---
description: Отображает диалоговое окно, позволяющее пользователям создавать, изменять и удалять профили сканирования.
ms.assetid: 208ec527-f7ad-4d45-b433-6d7d3658ca26
title: 'Метод Исканпрофилеуи:: Сканпрофиледиалог (Сканпрофилеуи. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileUI.ScanProfileDialog
api_type:
- COM
api_location:
- Scanprofileui.h
ms.openlocfilehash: a2003471a151677b5f0fbd9ae88e9d3cf8d975525a9dbf8340c6fc1a9f2befc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965813"
---
# <a name="iscanprofileuiscanprofiledialog-method"></a>Метод Исканпрофилеуи:: Сканпрофиледиалог

Отображает диалоговое окно, позволяющее пользователям создавать, изменять и удалять профили сканирования.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ScanProfileDialog(
  [in] HWND hwndParent
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хвндпарент* \[ окне\]
</dt> <dd>

Тип: **HWND**

Маркер родительского окна, которому принадлежит диалоговое окно.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

Диалоговое окно является модальным; пользователь не может переключиться на родительское окно, пока диалоговое окно не закроется.

Значения `<ProfileName>` элемента и `<WiaItem>` элемента можно изменить в диалоговом окне. `<Default>`Элемент можно добавить или удалить. Другие изменения профиля сканирования не могут быть сделаны в диалоговом окне.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                              |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                        |
| Header<br/>                   | <dl> <dt>Сканпрофилеуи. h</dt> </dl>  |
| IDL<br/>                      | <dl> <dt>Сканпрофилес. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**исканпрофилеуи**](-wia-iscanprofileui.md)
</dt> <dt>

[Схема профиля сканирования](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




