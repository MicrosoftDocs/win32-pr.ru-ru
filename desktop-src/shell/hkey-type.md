---
description: Эти типы данных можно использовать для указания типа значения реестра.
title: Типы данных реестра (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4185e7af-e1f0-40af-91c7-0ff7e27896ae
api_name:
- REG_BINARY
- REG_DWORD
- REG_QWORD
- REG_DWORD_LITTLE_ENDIAN
- REG_QWORD_LITTLE_ENDIAN
- REG_DWORD_BIG_ENDIAN
- REG_EXPAND_SZ
- REG_LINK
- REG_MULTI_SZ
- REG_NONE
- REG_RESOURCE_LIST
- REG_SZ
api_type:
- HeaderDef
api_location:
- Winnt.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4de4595b55716d58df04a598dd6ba298f22829d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "104998984"
---
# <a name="registry-data-types"></a>Типы данных реестра

Эти типы данных можно использовать для указания типа значения реестра.



| Константа                                                                                                                                                                                      | Описание                                                                                                                                                                                                                                                                                                                  |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="REG_BINARY"></span><span id="reg_binary"></span><dl> <dt>**\_двоичный файл REG**</dt> </dl>                                          | Двоичные данные в любой форме.<br/>                                                                                                                                                                                                                                                                                          |
| <span id="REG_DWORD"></span><span id="reg_dword"></span><dl> <dt>**REG \_ DWORD**</dt> </dl>                                             | 32-разрядное число.<br/>                                                                                                                                                                                                                                                                                                    |
| <span id="REG_QWORD"></span><span id="reg_qword"></span><dl> <dt>**REG \_ QWORD**</dt> </dl>                                             | 64-разрядное число.<br/>                                                                                                                                                                                                                                                                                                    |
| <span id="REG_DWORD_LITTLE_ENDIAN"></span><span id="reg_dword_little_endian"></span><dl> <dt>**REG \_ DWORD с \_ прямым \_ порядком байтов**</dt> </dl> | 32-разрядный номер в формате с прямым порядком байтов. Это эквивалентно **reg \_ DWORD**.<br/> В формате с прямым порядком байтов многобайтовый параметр хранится в памяти с наименьшего байта ("маленький конец") до самого большого байта. Например, значение 0x12345678 хранится как (0x78 0x56 0x34 0x12) в формате с прямым порядком байтов.<br/> |
| <span id="REG_QWORD_LITTLE_ENDIAN"></span><span id="reg_qword_little_endian"></span><dl> <dt>**REG с обратным \_ \_ \_ порядком байтов**</dt> </dl> | 64-разрядный номер в формате с прямым порядком байтов. Это эквивалентно **reg \_ QWORD**. <br/>                                                                                                                                                                                                                                   |
| <span id="REG_DWORD_BIG_ENDIAN"></span><span id="reg_dword_big_endian"></span><dl> <dt>**REG \_ байт с \_ обратным \_ порядком байтов**</dt> </dl>          | 32-разрядный номер в формате с обратным порядком байтов.<br/> В формате с обратным порядком байтов многобайтовый параметр хранится в памяти из самого длинного байта («Big-конец») до наименьшего байта. Например, значение 0x12345678 сохраняется как (0x12 0x34 0x56 0x78) в формате с обратным порядком байтов.<br/>                                                   |
| <span id="REG_EXPAND_SZ"></span><span id="reg_expand_sz"></span><dl> <dt>**\_распаковать \_ SZ**</dt> </dl>                                | Строка, завершающаяся нулем, которая содержит нераскрытные ссылки на переменные среды (например, "% PATH%"). Это будет строка в Юникоде или ANSI в зависимости от того, используются ли функции Юникода или ANSI.<br/>                                                                                                     |
| <span id="REG_LINK"></span><span id="reg_link"></span><dl> <dt>**Ссылка на REG \_**</dt> </dl>                                                | Символьная ссылка в Юникоде.<br/>                                                                                                                                                                                                                                                                                            |
| <span id="REG_MULTI_SZ"></span><span id="reg_multi_sz"></span><dl> <dt>**REG \_ Multi \_ SZ**</dt> </dl>                                   | Массив строк, заканчивающихся нулем, заканчивающихся двумя символами NULL.<br/>                                                                                                                                                                                                                                      |
| <span id="REG_NONE"></span><span id="reg_none"></span><dl> <dt>**REG \_ None**</dt> </dl>                                                | Нет определенного типа значения.<br/>                                                                                                                                                                                                                                                                                            |
| <span id="REG_RESOURCE_LIST"></span><span id="reg_resource_list"></span><dl> <dt>**\_список ресурсов \_ реестра**</dt> </dl>                    | Список ресурсов драйвера устройства.<br/>                                                                                                                                                                                                                                                                                      |
| <span id="REG_SZ"></span><span id="reg_sz"></span><dl> <dt>**REG \_ SZ**</dt> </dl>                                                      | Строка, завершающаяся символом NULL. Это будет строка в Юникоде или ANSI в зависимости от того, используются ли функции Юникода или ANSI.<br/>                                                                                                                                                                                          |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Файл Winnt. h</dt> </dl> |



 

 




