---
description: Задает сопоставление подобразца для образца, указывающего очищенные и зашифрованные байты в образце данных.
ms.assetid: E672F53D-2083-430B-90D2-A1DA482EF9E1
title: Атрибут MFSampleExtension_Encryption_SubSampleMappingSplit (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c90fb6ae22417f059bfa3268382877363178940
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719427"
---
# <a name="mfsampleextension_encryption_subsamplemappingsplit-attribute"></a>\_ \_ Атрибут Субсамплемаппингсплит Encryption мфсампликстенсион

Задает сопоставление подобразца для образца, указывающего очищенные и зашифрованные байты в образце данных.

## <a name="data-type"></a>Тип данных

**ОБЪЕКТЕ**

## <a name="remarks"></a>Комментарии

**Большой двоичный объект** должен содержать массив диапазонов байтов в виде DWORD, где каждый из двух значений DWORD делает набор. Первый DWORD в каждом наборе — это число байтов очистки, а второй DWORD набора — число зашифрованных байтов. Обратите внимание, что пара нулей не является допустимым набором (любое значение может быть равно 0, но не одновременно). Массив диапазонов байтов указывает, какие диапазоны следует расшифровывать, в том числе возможность дешифрования всего образца. Не рекомендуется устанавливать этот параметр в Clear Samples, хотя можно добиться того же результата, задав для него соответствующие значения.

## <a name="examples"></a>Примеры

В следующем примере показано, как задать \_ субсамплемаппингсплит шифрования мфсампликстенсион \_ .


```C++
// m_spSample is a IMFSample
// pdwSubSampleMap is a DWORD*
// dwSubSampleMapSize is a DWORD

m_spSample->SetBlob( MFSampleExtension_Encryption_SubSampleMappingSplit,
                    (BYTE*)pdwSubSampleMap, 
                    dwSubSampleMapSize * sizeof(DWORD) );
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows 8.1 \|\]<br/>                                |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2012 R2 \|\]<br/>                     |
| Header<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[\_KeyID содержимого \_ мфсампликстенсион](mfsampleextension-content-keyid.md)
</dt> </dl>

 

 




