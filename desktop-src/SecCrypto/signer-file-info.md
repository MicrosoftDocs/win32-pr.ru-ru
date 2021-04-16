---
description: Указывает файл для подписи.
ms.assetid: 5b45d855-ede8-43eb-9253-e3fe1716686b
title: Структура SIGNER_FILE_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_FILE_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 71e7c360d0034d9435386cf31579299c6d047131
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664386"
---
# <a name="signer_file_info-structure"></a>\_ \_ Структура сведений о файле подписывания

Структура **\_ \_ сведений о файле подписывания** указывает файл для подписи.

> [!Note]  
> Эта структура не определена ни в одном файле заголовка. Чтобы использовать эту структуру, необходимо определить ее самостоятельно, как показано в этом разделе.

 

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _SIGNER_FILE_INFO {
  DWORD   cbSize;
  LPCWSTR pwszFileName;
  HANDLE  hFile;
} SIGNER_FILE_INFO, *PSIGNER_FILE_INFO;
```



## <a name="members"></a>Члены

<dl> <dt>

**кбсизе**
</dt> <dd>

Размер структуры в байтах.

</dd> <dt>

**пвсзфиленаме**
</dt> <dd>

Указатель на строку, завершающуюся нулем, которая содержит имя файла для подписи.

</dd> <dt>

**hFile**
</dt> <dd>

Открытый обработчик для файла, указанного членом **пвсзфиленаме** . Если этот член содержит допустимый обработчик, этот маркер используется для доступа к файлу. Этому элементу можно присвоить **значение NULL**.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>          |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_сведения о субъекте ПОДписывания \_**](signer-subject-info.md)
</dt> </dl>

 

 




