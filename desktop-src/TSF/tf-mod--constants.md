---
title: Константы TF_MOD_ (Мсктф. h)
description: '\_ \_ Константы TF mod \ указывают модификаторы ключа в структуре TF \_ пресерведкэй.'
ms.assetid: 4642ef17-34bd-4482-a9e9-0fbed7b574b1
topic_type:
- apiref
api_name:
- TF_MOD_ALT
- TF_MOD_CONTROL
- TF_MOD_SHIFT
- TF_MOD_RALT
- TF_MOD_RCONTROL
- TF_MOD_RSHIFT
- TF_MOD_LALT
- TF_MOD_LCONTROL
- TF_MOD_LSHIFT
- TF_MOD_ON_KEYUP
- TF_MOD_IGNORE_ALL_MODIFIER
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e67e081d9a0f8714410861c7c36f9f751bad8d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071585"
---
# <a name="tf_mod_-constants"></a>TF \_ Mod \_ \* константы

\_ \_ \* Константы TF mod указывают модификаторы ключа в структуре [tf \_ пресерведкэй](/windows/desktop/api/Msctf/ns-msctf-tf_preservedkey) .



| Константа/значение                                                                                                                                                                                                                                                      | Описание                                                                                                                                                                          |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_MOD_ALT"></span><span id="tf_mod_alt"></span><dl> <dt>**Tf \_ MOD \_ ALT**</dt> <dt>0x0001</dt> </dl>                                                   | Нажата одна из клавиш ALT<br/>                                                                                                                                         |
| <span id="TF_MOD_CONTROL"></span><span id="tf_mod_control"></span><dl> <dt>**Tf \_ 0x0002 \_ элемента управления mod**</dt> <dt></dt> </dl>                                       | Нажата любая из клавиш CTRL<br/>                                                                                                                                        |
| <span id="TF_MOD_SHIFT"></span><span id="tf_mod_shift"></span><dl> <dt>**Tf \_ 0x0004 \_ сдвиг mod**</dt> <dt></dt> </dl>                                             | Нажата любая из клавиш SHIFT<br/>                                                                                                                                       |
| <span id="TF_MOD_RALT"></span><span id="tf_mod_ralt"></span><dl> <dt>**Tf \_ MOD \_ ралт**</dt> <dt>0x0008</dt> </dl>                                                | Нажата правая клавиша ALT<br/>                                                                                                                                              |
| <span id="TF_MOD_RCONTROL"></span><span id="tf_mod_rcontrol"></span><dl> <dt>**Tf \_ MOD \_ рконтрол**</dt> <dt>0x0010</dt> </dl>                                    | Нажата правая клавиша CTRL<br/>                                                                                                                                             |
| <span id="TF_MOD_RSHIFT"></span><span id="tf_mod_rshift"></span><dl> <dt>**Tf \_ MOD \_ ршифт**</dt> <dt>0x0020</dt> </dl>                                          | Нажата клавиша SHIFT справа<br/>                                                                                                                                            |
| <span id="TF_MOD_LALT"></span><span id="tf_mod_lalt"></span><dl> <dt>**Tf \_ MOD \_ лалт**</dt> <dt>0x0040</dt> </dl>                                                | Нажата левая клавиша ALT<br/>                                                                                                                                               |
| <span id="TF_MOD_LCONTROL"></span><span id="tf_mod_lcontrol"></span><dl> <dt>**Tf \_ MOD \_ лконтрол**</dt> <dt>0x0080</dt> </dl>                                    | Нажата левая клавиша CTRL<br/>                                                                                                                                              |
| <span id="TF_MOD_LSHIFT"></span><span id="tf_mod_lshift"></span><dl> <dt>**Tf \_ MOD \_ лшифт**</dt> <dt>0x0100</dt> </dl>                                          | Нажата клавиша SHIFT слева<br/>                                                                                                                                             |
| <span id="TF_MOD_ON_KEYUP"></span><span id="tf_mod_on_keyup"></span><dl> <dt>**Tf \_ MOD \_ для \_ KEYUP**</dt> <dt>0x0200</dt> </dl>                                   | Событие будет запущено при освобождении ключа. Без этого флага событие срабатывает при нажатии клавиши.<br/>                                                          |
| <span id="TF_MOD_IGNORE_ALL_MODIFIER"></span><span id="tf_mod_ignore_all_modifier"></span><dl> <dt>**Tf \_ 0x0400 \_ пропуск \_ всех \_ модификаторов mod**</dt> <dt></dt> </dl> | Состояние клавиш ALT, CTRL и SHIFT игнорируется. Это означает, что событие будет срабатывать при нажатии на виртуальный ключ независимо от того, какие клавиши-модификаторы нажаты.<br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                 |
| Распространяемые компоненты<br/>          | TSF 1,0 в Windows 2000 профессиональная<br/>                                      |
| Header<br/>                   | <dl> <dt>Мсктф. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Мсктф. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[TF \_ пресерведкэй](/windows/desktop/api/Msctf/ns-msctf-tf_preservedkey)
</dt> </dl>

 

 





