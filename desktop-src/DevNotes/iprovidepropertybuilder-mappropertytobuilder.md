---
description: Проверяет, связан ли конструктор с определенным свойством.
ms.assetid: 8fab2dc2-3549-4559-b704-6783d929274e
title: 'Метод Ипровидепропертибуилдер:: Маппропертитобуилдер'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IProvidePropertyBuilder.MapPropertyToBuilder
api_type:
- COM
api_location:
- Vsp.dll
ms.openlocfilehash: 5fa755449bfb97940235fe45f9e299aa828e6faa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665262"
---
# <a name="iprovidepropertybuildermappropertytobuilder-method"></a>Метод Ипровидепропертибуилдер:: Маппропертитобуилдер

Проверяет, связан ли конструктор с определенным свойством.

## <a name="syntax"></a>Синтаксис


```C++
void MapPropertyToBuilder(
  [in]          LONG   dispid,
  [out]         DWORD  *pdwCtlBldType,
  [out]         LPBSTR pbstrGuidBldr,
  [out, retval] LPBOOL builderAvailable
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*идентификатор DISPID* \[ окне\]
</dt> <dd>

Идентификатор DISPID рассматриваемого свойства.

</dd> <dt>

*пдвктлблдтипе* \[ заполняет\]
</dt> <dd>

Построитель для сопоставления. Этот параметр может быть сочетанием следующих значений.



| Значение                                                                                                                                                                                                                                                          | Значение                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span id="CTLBLDTYPE_FSTDPROPBUILDER"></span><span id="ctlbldtype_fstdpropbuilder"></span><dl> <dt>**Ктлблдтипе \_ ФСТДПРОПБУИЛДЕР**</dt> <dt>1</dt> </dl>    | Вызов стандартного системного конструктора (не поддерживается в Visual Studio).<br/> |
| <span id="CTLBLDTYPE_FINTERNALBUILDER"></span><span id="ctlbldtype_finternalbuilder"></span><dl> <dt>**Ктлблдтипе \_ ФИНТЕРНАЛБУИЛДЕР**</dt> <dt>2</dt> </dl> | Вызовите пользовательский сборщик.<br/>                                           |
| <span id="CTLBLDTYPE_EDITSOBJDIRECTLY"></span><span id="ctlbldtype_editsobjdirectly"></span><dl> <dt>**Ктлблдтипе \_ ЕДИТСОБЖДИРЕКТЛИ**</dt> <dt>4</dt> </dl> | Построитель изменяет объект. Это обычное поведение.<br/>              |



 

</dd> <dt>

*пбстргуидблдр* \[ заполняет\]
</dt> <dd>

Идентификатор GUID, определяющий построитель для этого свойства.

</dd> <dt>

*буилдераваилабле* \[ out, retval\]
</dt> <dd>

Этот параметр имеет **значение true** , если это свойство в настоящее время поддерживает построитель.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Vsp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ипровидепропертибуилдер**](iprovidepropertybuilder.md)
</dt> </dl>

 

 




