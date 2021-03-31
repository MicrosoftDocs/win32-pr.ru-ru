---
title: Сообщение HKM_SETRULES (Коммктрл. h)
description: Определяет недопустимые сочетания и сочетание модификатора по умолчанию для элемента управления горячего ключа.
ms.assetid: de3dd463-a534-4c7c-ae04-da80a3bff2ab
keywords:
- Элементы управления Windows для HKM_SETRULES сообщений
topic_type:
- apiref
api_name:
- HKM_SETRULES
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c33c0918a7bb44fdac9a1f2c60fdde8e06b5e679
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491187"
---
# <a name="hkm_setrules-message"></a>\_Сообщение ХКМ сетрулес

Определяет недопустимые сочетания и сочетание модификатора по умолчанию для элемента управления горячего ключа.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Массив флагов, задающих недопустимые сочетания клавиш. Этот параметр может быть сочетанием следующих значений:



| Значение                                                                                                                                                   | Значение                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| <span id="HKCOMB_A"></span><span id="hkcomb_a"></span><dl> <dt>**ХККОМБ \_ A**</dt> </dl>          | ALT<br/>             |
| <span id="HKCOMB_C"></span><span id="hkcomb_c"></span><dl> <dt>**ХККОМБ \_ C**</dt> </dl>          | CTRL<br/>            |
| <span id="HKCOMB_CA"></span><span id="hkcomb_ca"></span><dl> <dt>**\_ЦС хккомб**</dt> </dl>       | CTRL + ALT<br/>        |
| <span id="HKCOMB_NONE"></span><span id="hkcomb_none"></span><dl> <dt>**ХККОМБ \_ None**</dt> </dl> | Неизмененные ключи<br/> |
| <span id="HKCOMB_S"></span><span id="hkcomb_s"></span><dl> <dt>**ХККОМБ \_ S**</dt> </dl>          | МЕСТИ<br/>           |
| <span id="HKCOMB_SA"></span><span id="hkcomb_sa"></span><dl> <dt>**ХККОМБ \_ SA**</dt> </dl>       | SHIFT + ALT<br/>       |
| <span id="HKCOMB_SC"></span><span id="hkcomb_sc"></span><dl> <dt>**ХККОМБ \_ SC**</dt> </dl>       | SHIFT + CTRL<br/>      |
| <span id="HKCOMB_SCA"></span><span id="hkcomb_sca"></span><dl> <dt>**ХККОМБ \_ SCA**</dt> </dl>    | SHIFT + CTRL + ALT<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Массив флагов, указывающих сочетание клавиш, которое будет использоваться при вводе пользователем недопустимого сочетания. Список значений флагов модификаторов см. в описании сообщения ХКМ- [**\_ горячих клавиш**](hkm-gethotkey.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Комментарии

Когда пользователь вводит недопустимое сочетание клавиш, как определено флагами, указанными в параметре *wParam*, система использует оператор побитового или для объединения вводимых пользователем ключей с флагами, указанными в параметре *lParam*. Полученное сочетание клавиш преобразуется в строку и затем отображается в элементе управления "горячая клавиша".

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





