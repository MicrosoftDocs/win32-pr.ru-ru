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
ms.openlocfilehash: eae1a46b43278c836ff6ce318dfdce7302bb0e052664a7326f9043a60eec72d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118905633"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista с пакетом обновления 1 (SP1), \[ только классические приложения\]<br/>                                                                                                                                                                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                                                                                                                                                                           |
| DLL<br/>                      | <dl> <dt>Ksecdd.sys на Windows Server 2008 и Windows Vista с пакетом обновления 1 (SP1);</dt> <dt>Cng.sys на Windows 7 и Windows Server 2008 R2</dt> </dl> |



 

 




