---
title: Структура ВМДМИД
description: Структура ВМДМИД описывает серийные номера и идентификаторы групп.
ms.assetid: eaa5786e-a2a1-42d7-b527-be83d944cb20
keywords:
- Структура ВМДМИД Windows Media диспетчер устройств
- Указатель структуры ПВМДМИД Windows Media диспетчер устройств
topic_type:
- apiref
api_name:
- WMDMID
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8edc2a364bf29ead6aaf4fad8ad3a56fe80d7176
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699126"
---
# <a name="wmdmid-structure"></a>Структура ВМДМИД

Структура **вмдмид** описывает серийные номера и идентификаторы групп.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct __WMDMID {
  UINT  cbSize;
  DWORD dwVendorID;
  BYTE  pID[WMDMID_LENGTH];
  UINT  SerialNumberLength;
} WMDMID, *PWMDMID;
```



## <a name="members"></a>Члены

<dl> <dt>

**кбсизе**
</dt> <dd>

Размер структуры **вмдмид** в байтах.

</dd> <dt>

**дввендорид**
</dt> <dd>

Значение **типа DWORD** , содержащее зарегистрированный идентификатор поставщика. Содержит ноль, если не используется.

</dd> <dt>

**\[Длина pID вмдмид \_\]**
</dt> <dd>

Указатель на массив байтов, содержащий серийный номер. Серийный номер — это строка байтовых значений, не имеющая стандартного формата. Обратите внимание, что это значение не является расширенным символом. **Вмдмид \_ LENGTH** — это постоянное значение, определенное в мсвмдм. h.

</dd> <dt>

**сериалнумберленгс**
</dt> <dd>

Фактическая длина возвращенного серийного номера в байтах.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Вмдм. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Имдспдевице:: Жетсериалнумбер**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-getserialnumber)
</dt> <dt>

[**Имдспсторажеглобалс:: Жетсериалнумбер**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getserialnumber)
</dt> <dt>

[**Ивмдмдевице:: Жетсериалнумбер**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getserialnumber)
</dt> <dt>

[**Ивмдмсторажеглобалс:: Жетсериалнумбер**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-getserialnumber)
</dt> <dt>

[**Структуры**](structures.md)
</dt> </dl>

 

 





