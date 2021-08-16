---
title: Сообщение HKM_SETRULES (Коммктрл. h)
description: Определяет недопустимые сочетания и сочетание модификатора по умолчанию для элемента управления горячего ключа.
ms.assetid: de3dd463-a534-4c7c-ae04-da80a3bff2ab
keywords:
- элементы управления Windows сообщений HKM_SETRULES
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
ms.openlocfilehash: 4ec47450ca0d67854d7be413d8a3eb3e5fec3eac49e18f6bcf96f86b563c8906
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958713"
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

## <a name="remarks"></a>Remarks

Когда пользователь вводит недопустимое сочетание клавиш, как определено флагами, указанными в параметре *wParam*, система использует оператор побитового или для объединения вводимых пользователем ключей с флагами, указанными в параметре *lParam*. Полученное сочетание клавиш преобразуется в строку и затем отображается в элементе управления "горячая клавиша".

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





