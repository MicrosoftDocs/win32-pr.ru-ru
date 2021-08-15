---
description: Структура ЕКСПЕРТФРАМЕДЕСКРИПТОР содержит сведения о кадре. Когда эксперт успешно вызывает функцию Експертжетфраме, сетевой монитор передает структуру ЕКСПЕРТФРАМЕДЕСКРИПТОР обратно эксперту.
ms.assetid: 6cf99498-3cf9-46da-b6a0-3012229f6908
title: Структура ЕКСПЕРТФРАМЕДЕСКРИПТОР (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTFRAMEDESCRIPTOR
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 4a11c131188cdd5230d309a6ff2e39a77ac7886333dafd9860d565fdcb10efc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939031"
---
# <a name="expertframedescriptor-structure"></a>Структура ЕКСПЕРТФРАМЕДЕСКРИПТОР

Структура **експертфрамедескриптор** содержит сведения о кадре. Когда эксперт успешно вызывает функцию [**експертжетфраме**](expertgetframe.md) , сетевой монитор передает структуру **експертфрамедескриптор** обратно эксперту.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct {
  DWORD                FrameNumber;
  HFRAME               hFrame;
  ULPFRAME             pFrame;
  LPRECOGNIZEDATATABLE lpRecognizeDataTable;
  LPPROPERTYTABLE      lpPropertyTable;
} EXPERTFRAMEDESCRIPTOR, *LPEXPERTFRAMEDESCRIPTOR;
```



## <a name="members"></a>Члены

<dl> <dt>

**фраменумбер**
</dt> <dd>

Номер указанного кадра.

</dd> <dt>

**хфраме**
</dt> <dd>

Обработчик для фрейма.

</dd> <dt>

**пфраме**
</dt> <dd>

Указатель на необработанный кадр.

</dd> <dt>

**лпрекогнизедататабле**
</dt> <dd>

Таблица, указывающая, где каждый синтаксический анализатор определяет начало данных.

</dd> <dt>

**лппропертитабле**
</dt> <dd>

Таблица свойств кадра, идентифицируемая синтаксическим анализатором.

</dd> </dl>

## <a name="remarks"></a>Remarks

Если эксперт задает ФЛАГи \_ присоединения \_ свойств при вызове [**експертжетфраме**](expertgetframe.md), то элемент **сзпропертитекст** в каждой структуре [**пропертинст**](propertyinst.md) имеет **значение NULL**.

Если эксперт не задает ФЛАГи \_ присоединения \_ свойств при вызове функции [**експертжетфраме**](expertgetframe.md) , то элемент **лппропертитабле** имеет **значение NULL** при возврате.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




