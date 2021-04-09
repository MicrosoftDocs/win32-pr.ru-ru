---
description: Указывает, какие байты зашифрованы в защищенной видеоповерхности.
ms.assetid: 076f4f00-e86b-47e2-80dd-4d7434200138
title: Структура D3DENCRYPTED_BLOCK_INFO (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DENCRYPTED_BLOCK_INFO
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 21864dcc41ce86f139361af4357810137acf7f06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143153"
---
# <a name="d3dencrypted_block_info-structure"></a>\_ \_ Структура сведений о БЛОКе D3DENCRYPTED

Указывает, какие байты зашифрованы в защищенной видеоповерхности.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _D3DENCRYPTED_BLOCK_INFO {
  UINT NumEncryptedBytesAtBeginning;
  UINT NumBytesInSkipPattern;
  UINT NumBytesInEncryptPattern;
} D3DENCRYPTED_BLOCK_INFO;
```



## <a name="members"></a>Члены

<dl> <dt>

**нуменкриптедбитесатбегиннинг**
</dt> <dd>

Число байтов, зашифрованных в начале буфера.

</dd> <dt>

**нумбитесинскиппаттерн**
</dt> <dd>

Число байтов, пропущенных после первого **нуменкриптедбитесатбегиннинг** байт, а затем после каждого блока **нумбитесиненкриптпаттерн** байт. Пропущенные байты не шифруются.

</dd> <dt>

**нумбитесиненкриптпаттерн**
</dt> <dd>

Число байтов, зашифрованных после каждого блока пропущенных байтов.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                                              |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>D3d9types. h (включение D3d9. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Видеоструктуры Direct3D](direct3d-video-structures.md)
</dt> </dl>

 

 




