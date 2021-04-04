---
description: Задает атрибуты для подписи Authenticode.
ms.assetid: 1c1052c3-c5c5-48ae-8266-0b367800a84a
title: Структура SIGNER_ATTR_AUTHCODE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_ATTR_AUTHCODE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 952ed0f55a185d9a7ef9eeed3366f64c84423ddd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999658"
---
# <a name="signer_attr_authcode-structure"></a>Двухфакторной, подпись \_ attr, \_ Структура

**\_ \_ Двухфакторнойная структура attr** определяет атрибуты для подписи [*Authenticode*](../secgloss/a-gly.md) .

> [!Note]  
> Эта структура не определена ни в одном файле заголовка. Чтобы использовать эту структуру, необходимо определить ее самостоятельно, как показано в этом разделе.

 

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _SIGNER_ATTR_AUTHCODE {
  DWORD   cbSize;
  BOOL    fCommercial;
  BOOL    fIndividual;
  LPCWSTR pwszName;
  LPCWSTR pwszInfo;
} SIGNER_ATTR_AUTHCODE, *PSIGNER_ATTR_AUTHCODE;
```



## <a name="members"></a>Члены

<dl> <dt>

**кбсизе**
</dt> <dd>

Размер структуры в байтах.

</dd> <dt>

**фкоммерЦиал**
</dt> <dd>

**Значение true** , чтобы подписать субъект в качестве коммерческого издателя; в противном случае — **значение false**.

</dd> <dt>

**финдивидуал**
</dt> <dd>

**Значение true** , чтобы подписать тему как отдельный издатель; в противном случае — **значение false**.

</dd> <dt>

**pwszName**
</dt> <dd>

Отображаемое имя файла при скачивании.

</dd> <dt>

**пвсзинфо**
</dt> <dd>

Отображаемое имя URL-адреса файла при скачивании.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>          |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_сведения о подписи ПОДписывания \_**](signer-signature-info.md)
</dt> </dl>

 

 
