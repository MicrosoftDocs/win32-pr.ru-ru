---
title: Структура ВМФИЛЕКАПАБИЛИТИЕС
description: Структура ВМФИЛЕКАПАБИЛИТИЕС описывает тип MIME.
ms.assetid: 30307343-f55e-4695-9ae8-b938617d749d
keywords:
- Структура ВМФИЛЕКАПАБИЛИТИЕС Windows Media диспетчер устройств
topic_type:
- apiref
api_name:
- WMFILECAPABILITIES
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc7657ddd15a4219a0d5f56dbadeffba2a9547bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694546"
---
# <a name="wmfilecapabilities-structure"></a>Структура ВМФИЛЕКАПАБИЛИТИЕС

Структура **вмфилекапабилитиес** описывает тип MIME.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _tagWMFILECAPABILITIES {
  LPWSTR pwszMimeType;
  DWORD  dwReserved;
} WMFILECAPABILITIES;
```



## <a name="members"></a>Члены

<dl> <dt>

**пвсзмиметипе**
</dt> <dd>

Тип MIME.

</dd> <dt>

**двресервед**
</dt> <dd>

**DWORD** зарезервировано для будущего использования. Установите нулевое значение (0).

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Вмдм. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IWMDMDevice2::GetFormatSupport2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getformatsupport2)
</dt> <dt>

[**Структуры**](structures.md)
</dt> </dl>

 

 





