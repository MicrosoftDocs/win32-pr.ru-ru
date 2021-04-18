---
description: Извлекает указанное число случайных байтов из системного генератора случайных чисел.
ms.assetid: 04746229-9dc1-4748-80c1-f1960bd1b768
title: Функция SystemPrng
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemPrng
api_type:
- DllExport
api_location:
- Ksecdd.sys
- Cng.sys
ms.openlocfilehash: d847d34ffd11e158170f55599de0ceb3acf3c697
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662331"
---
# <a name="systemprng-function"></a>Функция SystemPrng

\[**SystemPrng** доступен для использования в операционных системах, указанных в разделе требования. В последующих версиях он может быть изменен или недоступен. Вместо этого используйте [**BCryptGenRandom**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgenrandom).\]

Функция **SystemPrng** извлекает указанное число случайных байтов из системного генератора случайных чисел.

> [!Note]  
> Эта функция не имеет связанного файла заголовка или библиотеки импорта. Чтобы вызвать эту функцию, необходимо создать файл заголовка, определяемый пользователем.

 

## <a name="syntax"></a>Синтаксис


```C++
BOOL SystemPrng(
  _Out_ unsigned char pbRandomData,
  _In_  size_t        cbRandomData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пбрандомдата* \[ заполняет\]
</dt> <dd>

Указатель на буфер, который получает извлеченные байты.

</dd> <dt>

*кбрандомдата* \[ окне\]
</dt> <dd>

Число извлекаемых байтов.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Всегда возвращает **значение true**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для настольных приложений Windows Vista с пакетом обновления 1 \[\]<br/>                                                                                                                                                                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                                                                                                                                                                           |
| DLL<br/>                      | <dl> <dt>Ksecdd.sys в Windows Server 2008 и Windows Vista с пакетом обновления 1 (SP1); </dt> <dt>Cng.sys в Windows 7 и Windows Server 2008 R2</dt> </dl> |



 

 




