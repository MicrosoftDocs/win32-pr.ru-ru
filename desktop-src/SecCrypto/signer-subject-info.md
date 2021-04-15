---
description: Указывает тему для подписи.
ms.assetid: ba569443-e50f-450b-82cc-b7328f0ca25a
title: Структура SIGNER_SUBJECT_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_SUBJECT_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 05b5d780e50f8ea10fcf68cc90ae7092bbc2c473
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662887"
---
# <a name="signer_subject_info-structure"></a>\_Структура сведений о субъекте ПОДписывания \_

В структуре **\_ \_ сведений о субъекте-подписывания** указана тема для подписания.

> [!Note]  
> Эта структура не определена ни в одном файле заголовка. Чтобы использовать эту структуру, необходимо определить ее самостоятельно, как показано в этом разделе.

 

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _SIGNER_SUBJECT_INFO {
  DWORD cbSize;
  DWORD *pdwIndex;
  DWORD dwSubjectChoice;
  union {
    SIGNER_FILE_INFO *pSignerFileInfo;
    SIGNER_BLOB_INFO *pSignerBlobInfo;
  };
} SIGNER_SUBJECT_INFO, *PSIGNER_SUBJECT_INFO;
```



## <a name="members"></a>Члены

<dl> <dt>

**кбсизе**
</dt> <dd>

Размер структуры в байтах.

</dd> <dt>

**пдвиндекс**
</dt> <dd>

Этот член зарезервирован. Он должен иметь значение 0.

</dd> <dt>

**двсубжектчоице**
</dt> <dd>

Указывает, является ли субъект файлом или BLOB- [*объектом*](../secgloss/b-gly.md). Этот элемент может иметь одно или несколько следующих значений.



| Значение                                                                                                                                                                                                                                         | Значение                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="SIGNER_SUBJECT_BLOB"></span><span id="signer_subject_blob"></span><dl> <dt>**\_ Подписавший \_BLOB-объект темы**</dt> <dt>2 (0x2)</dt> </dl> | Субъект — это большой двоичный объект.<br/> |
| <span id="SIGNER_SUBJECT_FILE"></span><span id="signer_subject_file"></span><dl> <dt>**\_ Подписавший \_Файл темы**</dt> <dt>1 (0x1)</dt> </dl> | Субъект — это файл.<br/> |



 

</dd> <dt>

**псигнерфилеинфо**
</dt> <dd>

Указатель на [**\_ \_ информационную структуру файла подписи**](signer-file-info.md) , указывающий файл для подписи.

</dd> <dt>

**псигнерблобинфо**
</dt> <dd>

Указатель на структуру [**\_ \_ сведений о большом двоичном объекте**](signer-blob-info.md) , указывающий BLOB-объект для подписи.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>          |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**сигнерсигн**](signersign.md)
</dt> <dt>

[**сигнерсигнекс**](signersignex.md)
</dt> </dl>

 

 
