---
title: Структура WM_INDIVIDUALIZE_STATUS (Вмдрмсдк. h)
description: '\_ \_ Структура состояния WM индивидуализируйте содержит сведения о ожидающем процессе индивидуализации.'
ms.assetid: af7e8758-489b-461f-b241-d7e40c8d61da
keywords:
- Формат WM_INDIVIDUALIZE_STATUS структуры Windows Media
topic_type:
- apiref
api_name:
- WM_INDIVIDUALIZE_STATUS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c139631fe737e07d011e43920ab63c7394f03c3319abb2f7936153ae06c596ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119708304"
---
# <a name="wm_individualize_status-structure-wmdrmsdkh"></a>Структура WM_INDIVIDUALIZE_STATUS (Вмдрмсдк. h)

Структура **\_ \_ состояния WM индивидуализируйте** содержит сведения о ожидающем процессе индивидуализации.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _WMIndividualizeStatus {
  HRESULT                      hr;
  DRM_INDIVIDUALIZATION_STATUS enIndiStatus;
  LPSTR                        pszIndiRespUrl;
  DWORD                        dwHTTPRequest;
  DRM_HTTP_STATUS              enHTTPStatus;
  DWORD                        dwHTTPReadProgress;
  DWORD                        dwHTTPReadTotal;
} WM_INDIVIDUALIZE_STATUS;
```



## <a name="members"></a>Члены

<dl> <dt>

**ч**
</dt> <dd>

Код возврата **HRESULT** .

</dd> <dt>

**ениндистатус**
</dt> <dd>

Значение из типа перечисления " [**\_ \_ состояние индивидуальной обработки DRM**](drmdrm-individualization-status.md) ", которое указывает текущее состояние процесса индивидуализации.

</dd> <dt>

**псзиндиреспурл**
</dt> <dd>

Указатель на строку с завершающим нулем, содержащую URL-адрес ответа для индивидуальной строки.

</dd> <dt>

**двхттпрекуест**
</dt> <dd>

Количество полных путей HTTP к службе индивидуализации, которые были завершены.

</dd> <dt>

**енхттпстатус**
</dt> <dd>

Значение из типа [**перечисления \_ \_ состояния HTTP DRM**](drmdrm-http-status.md) .

</dd> <dt>

**двхттпреадпрогресс**
</dt> <dd>

Число скачанных байтов.

</dd> <dt>

**двхттпреадтотал**
</dt> <dd>

Общее число байтов для загрузки. Вы можете использовать это значение и **двхттпреадпрогресс** , чтобы отобразить пользовательский интерфейс, указывающий, сколько завершенных Скачиваний и сколько осталось выполнить.

</dd> </dl>

## <a name="remarks"></a>Remarks

Эта структура получается при вызове метода [**ивмдрминдивидуализатионстатус::-Status**](iwmdrmindividualizationstatus-getstatus.md) . Он содержит состояние ожидающего процесса индивидуализации во время вызова.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Вмдрмсдк. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Структуры**](drm-structures.md)
</dt> </dl>

 

 





