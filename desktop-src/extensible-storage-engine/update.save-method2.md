---
description: Дополнительные сведения см. в статье метод обновления. Save.
title: Метод Update. Save
TOCTitle: 'Save method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Update.Save
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.update.save(v=EXCHG.10)
ms:contentKeyID: 55104195
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Update.Save
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 75927144f887ab5cd7dbfe05c6d8fbf4c690a0e29786c1834fa00f8e29fae76c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117890065"
---
# <a name="updatesave-method"></a>Метод Update. Save

Обновите TableID.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Sub Save
'Usage
Dim instance As Update

instance.Save()
```

``` csharp
public void Save()
```

## <a name="remarks"></a>Remarks

Сохранение является последним шагом в выполнении вставки или обновления. Обновление начинается с вызова метода создания объекта Update, а затем путем вызова Жетсетколумн или Жетсетколумнс один или несколько раз для задания состояния записи. Наконец, для завершения операции обновления вызывается обновление. Индексы обновляются только с помощью Update, а не во время Жетсетколумн или Жетсетколумнс.

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс обновления](./update-class.md)

[Обновить элементы](./update-members.md)

[Сохранить перегрузку](./update.save-method.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
