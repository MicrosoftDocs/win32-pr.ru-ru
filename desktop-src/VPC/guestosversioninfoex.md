---
title: Структура ГУЕСТОСВЕРСИОНИНФОЕКС (Впккоминтерфацес. h)
description: Содержит сведения о версии операционной системы для гостевой операционной системы.
ms.assetid: 9cfd5cac-c8ea-4e09-ba47-3563554bdafa
keywords:
- Структура ГУЕСТОСВЕРСИОНИНФОЕКС Virtual PC
topic_type:
- apiref
api_name:
- GUESTOSVERSIONINFOEX
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 848196448c2bd6f021d85f7c13972e81664dd60a0e4a0bbbd2e05ef3455aade7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056912"
---
# <a name="guestosversioninfoex-structure"></a>Структура ГУЕСТОСВЕРСИОНИНФОЕКС

\[Windows Virtual PC больше не доступен для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Содержит сведения о версии операционной системы для гостевой операционной системы.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _GUESTOSVERSIONINFOEX {
  long    dwOSVersionInfoSize;
  long    dwMajorVersion;
  long    dwMinorVersion;
  long    dwBuildNumber;
  long    dwPlatformId;
  wchar_t szCSDVersion[128];
  short   wServicePackMajor;
  short   wServicePackMinor;
  short   wSuiteMask;
  byte    wProductType;
  byte    wReserved;
} GUESTOSVERSIONINFOEX;
```



## <a name="members"></a>Члены

<dl> <dt>

**двосверсионинфосизе**
</dt> <dd>

Размер этой структуры данных в байтах. Присвойте этому элементу значение `sizeof(GUESTOSVERSIONINFOEX)` .

</dd> <dt>

**двмажорверсион**
</dt> <dd>

Основной номер версии.

</dd> <dt>

**двминорверсион**
</dt> <dd>

Дополнительный номер версии.

</dd> <dt>

**двбуилднумбер**
</dt> <dd>

Номер сборки.

</dd> <dt>

**двплатформид**
</dt> <dd>

Платформа операционной системы. Этот член может быть **\_ платформой версии \_ Win32 \_ NT** (2).

</dd> <dt>

**сзксдверсион**
</dt> <dd>

Строка, завершающаяся нулем, например "пакет обновления 3", которая указывает на последний установленный в системе пакет обновления. Если пакет обновления не установлен, строка пуста.

</dd> <dt>

**всервицепаккмажор**
</dt> <dd>

Основной номер версии последнего установленного пакета обновления.

</dd> <dt>

**всервицепаккминор**
</dt> <dd>

Дополнительный номер версии последнего установленного пакета обновления.

</dd> <dt>

**всуитемаск**
</dt> <dd>

Битовая маска, определяющая наборы продуктов, доступные в системе. Этот элемент может быть сочетанием следующих значений.



| Значение                                                                                                                                                                                                                                                                                          | Значение                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VER_SUITE_BACKOFFICE"></span><span id="ver_suite_backoffice"></span><dl> <dt>**Версия \_ НАБОР \_ BackOffice**</dt> <dt>0x00000004</dt> </dl>                                            | Компоненты Microsoft BackOffice установлены.<br/>                                                                                                                                                         |
| <span id="VER_SUITE_BLADE"></span><span id="ver_suite_blade"></span><dl> <dt>**Версия \_ \_Колонка "набор**</dt> " <dt>0x00000400</dt> </dl>                                                           | Windows Установлен сервер 2003, Web Edition.<br/>                                                                                                                                                         |
| <span id="VER_SUITE_COMPUTE_SERVER"></span><span id="ver_suite_compute_server"></span><dl> <dt>**Версия \_ НАБОР \_ вычислений для \_ сервера**</dt> <dt>0x00004000</dt> </dl>                               | Windows Сервер 2003, установлен выпуск Compute Cluster Edition.<br/>                                                                                                                                             |
| <span id="VER_SUITE_DATACENTER"></span><span id="ver_suite_datacenter"></span><dl> <dt>**Версия \_ 0x00000080 \_ центра данных набора**</dt> <dt></dt> </dl>                                            | Windows установлен сервер 2008 datacenter, Windows server 2003, datacenter Edition или Windows 2000 datacenter Server.<br/>                                                                               |
| <span id="VER_SUITE_ENTERPRISE"></span><span id="ver_suite_enterprise"></span><dl> <dt>**Версия \_ Комплект \_ Enterprise**</dt> <dt>0x00000002</dt> </dl>                                            | Windows установлен сервер 2008 Enterprise, Windows server 2003, выпуск Enterprise или Windows 2000 Advanced Server. Дополнительные сведения об этом битовом флаге см. в разделе "Примечания".<br/>          |
| <span id="VER_SUITE_EMBEDDEDNT"></span><span id="ver_suite_embeddednt"></span><dl> <dt>**Версия \_ 0x00000040 \_ ЕМБЕДДЕДНТ Suite**</dt> <dt></dt> </dl>                                            | Windows Установлен XP Embedded.<br/>                                                                                                                                                                      |
| <span id="VER_SUITE_PERSONAL"></span><span id="ver_suite_personal"></span><dl> <dt>**Версия \_ \_Персональный**</dt> <dt>0x00000200</dt> Suite </dl>                                                  | Windows установлена домашняя Premium Vista, Windows vista home Basic или Windows XP home Edition.<br/>                                                                                                         |
| <span id="VER_SUITE_SINGLEUSERTS"></span><span id="ver_suite_singleuserts"></span><dl> <dt>**Версия \_ 0x00000100 \_ СИНГЛЕУСЕРТС Suite**</dt> <dt></dt> </dl>                                      | Удаленный рабочий стол поддерживается, но поддерживается только один интерактивный сеанс. Это значение задается, если система не работает в режиме сервера приложений.<br/>                                                 |
| <span id="VER_SUITE_SMALLBUSINESS"></span><span id="ver_suite_smallbusiness"></span><dl> <dt>**Версия \_ НАБОР \_ смаллбусинесс**</dt> <dt>0x00000001</dt> </dl>                                   | Microsoft Small Business Server был установлен в системе, но может быть обновлен до другой версии Windows. Дополнительные сведения об этом битовом флаге см. в разделе "Примечания".<br/>     |
| <span id="VER_SUITE_SMALLBUSINESS_RESTRICTED"></span><span id="ver_suite_smallbusiness_restricted"></span><dl> <dt>**Версия \_ \_СМАЛЛБУСИНЕСС Suite \_ ограниченный**</dt> <dt>0x00000020</dt> </dl> | Microsoft Small Business Server устанавливается с лицензией на клиентскую лицензию принудительно. Дополнительные сведения об этом битовом флаге см. в разделе "Примечания".<br/>                                      |
| <span id="VER_SUITE_STORAGE_SERVER"></span><span id="ver_suite_storage_server"></span><dl> <dt>**Версия \_ 0x00002000 \_ \_ сервера хранилища Suite**</dt> <dt></dt> </dl>                               | установлен Windows служба хранилища server 2003 R2 или Windows служба хранилища server 2003.<br/>                                                                                                                             |
| <span id="VER_SUITE_TERMINAL"></span><span id="ver_suite_terminal"></span><dl> <dt>**Версия \_ \_Терминальный пакет**</dt> <dt>0x00000010</dt> </dl>                                                  | Службы терминалов установлены. Это значение всегда задано.<br/> Если **установлен \_ \_ терминал ver Suite** , но версия **ver \_ Suite \_ синглеусертс** не задана, система работает в режиме сервера приложений.<br/> |
| <span id="VER_SUITE_WH_SERVER"></span><span id="ver_suite_wh_server"></span><dl> <dt>**Версия \_ НАБОР \_ \_**</dt> , который является <dt>0x00008000ом</dt> сервера </dl>                                              | Windows Установлен домашний сервер.<br/>                                                                                                                                                                      |



 

</dd> <dt>

**впродукттипе**
</dt> <dd>

Дополнительные сведения о системе. Этот элемент может принимать одно из следующих значений.



| Значение                                                                                                                                                                                                                                                           | Значение                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VER_NT_DOMAIN_CONTROLLER"></span><span id="ver_nt_domain_controller"></span><dl> <dt>**Версия \_ \_ \_ Контроллер домена NT**</dt> <dt>0x0000002</dt> </dl> | система является контроллером домена, а операционная система — Windows server 2008 r2, Windows server 2008, Windows server 2003 r2, Windows server 2003 или Windows 2000 server.<br/>                                                                                                   |
| <span id="VER_NT_SERVER"></span><span id="ver_nt_server"></span><dl> <dt>**Версия \_ NT \_ Server**</dt> <dt>0x0000003</dt> </dl>                                   | операционная система — Windows server 2008 r2, Windows server 2008, Windows server 2003 R2, Windows server 2003 или Windows 2000 server.<br/> Обратите внимание, что сервер, который также является контроллером домена, сообщается как **\_ \_ \_ контроллер домена ver NT**, а не **\_ \_ сервер ver NT**.<br/> |
| <span id="VER_NT_WORKSTATION"></span><span id="ver_nt_workstation"></span><dl> <dt>**Версия \_ \_Рабочая станция NT**</dt> <dt>0x0000001</dt> </dl>                    | операционная система — Windows 7, Windows Vista, Windows XP или Windows 2000 Professional.<br/>                                                                                                                                                                                       |



 

</dd> <dt>

**вресервед**
</dt> <dd>

Зарезервировано для последующего использования.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Заголовок<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Ивмгуестос:: Жетосверсионинфо**](ivmguestos-getosversioninfo.md)
</dt> </dl>

 

