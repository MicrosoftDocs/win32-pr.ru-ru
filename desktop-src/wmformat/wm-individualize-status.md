---
title: Структура WM_INDIVIDUALIZE_STATUS (Дрмекстерналс. h)
description: '\_ \_ Структура состояния WM индивидуализируйте записывает состояние процесса индивидуализации.'
ms.assetid: 3779ed6f-c133-4a9d-b60c-ef8c41fcc4af
keywords:
- Формат WM_INDIVIDUALIZE_STATUS структуры Windows Media
topic_type:
- apiref
api_name:
- WM_INDIVIDUALIZE_STATUS
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb083c2a90a791099f6438f2911ac9735ecd4dada9118811aa0ff581a8db37ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118699024"
---
# <a name="wm_individualize_status-structure-drmexternalsh"></a>Структура WM_INDIVIDUALIZE_STATUS (Дрмекстерналс. h)

Структура **\_ \_ состояния WM индивидуализируйте** записывает состояние процесса [*индивидуализации*](wmformat-glossary.md) .

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

Значение из типа перечисления " [**\_ \_ состояние индивидуализации" DRM**](drm-individualization-status.md) .

</dd> <dt>

**псзиндиреспурл**
</dt> <dd>

Указатель на строку с завершающим нулем, содержащую URL-адрес ответа для индивидуальной строки.

</dd> <dt>

**двхттпрекуест**
</dt> <dd>

**Параметр DWORD** , указывающий количество выполненных циклов HTTP-обращений к службе индивидуализации.

</dd> <dt>

**енхттпстатус**
</dt> <dd>

Значение из типа [**перечисления \_ \_ состояния HTTP DRM**](drm-http-status.md) .

</dd> <dt>

**двхттпреадпрогресс**
</dt> <dd>

Значение **типа DWORD** , содержащее число байтов, скачанных до настоящего момента.

</dd> <dt>

**двхттпреадтотал**
</dt> <dd>

Значение **типа DWORD** , содержащее общее число байтов для загрузки. Используйте это значение и **двхттпреадпрогресс** , чтобы отобразить пользовательский интерфейс, указывающий, сколько завершенных Скачиваний и сколько осталось выполнить.

</dd> </dl>

## <a name="remarks"></a>Remarks

Эта структура заполняется компонентами времени выполнения DRM и отправляется в приложения в параметре *pValue* метода [**ивмстатускаллбакк:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) , если событие равно ВМТ \_ индивидуализируйте. Приложение получает это событие несколько раз во время процесса загрузки.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                      |
| Версия<br/>                  | Windows Пакет SDK для формата мультимедиа 7 или более поздние версии пакета SDK<br/>                       |
| Header<br/>                   | <dl> <dt>Дрмекстерналс. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_состояние HTTP \_ DRM**](drm-http-status.md)
</dt> <dt>

[**Структуры**](structures.md)
</dt> </dl>

 

 





